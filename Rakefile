require 'treebank/transform'
require 'fileutils'


#################
#  Log Helpers  #
#################

def colorize(str, color)
  "\e[#{color}m#{str}\e[0m"
end

def log(message, color, delimit = false)
  if delimit
    padded = "# #{message} #"
    delimiter = padded.each_char.map { '#' }.join
    ['', delimiter, padded, delimiter, ''].each do |str|
      puts colorize(str, color)
    end
  else
    puts colorize(message, color)
  end
end

def info(message, delimit = false)
  log(message, 33, delimit)
end

def success(message, delimit = false)
  log(message, 32, delimit)
end


##################
#  File Helpers  #
##################

TB_EXTENSION = '.tb.xml'
XML_EXTENSION = '.xml'
TEMP_EXTENSION = ".tmp.xml"
TEMP_PATH = "temp_transformations"
V1_TO_IGNORE = %w{ ldt-1.5 agdt-1.7 }

def v1_path(lang)
  File.join('v1', lang, 'data')
end

def v1six_path(lang)
  File.join('v1.6', lang, 'data')
end

def xml_glob_at(path)
  File.join(path, "*#{XML_EXTENSION}")
end

def temp_file(filename)
  stripped = File.basename(filename, XML_EXTENSION)
  "#{stripped}#{TEMP_EXTENSION}"
end

def temp_dir(lang)
  File.join(TEMP_PATH, lang)
end


###########
#  Tasks  #
###########

desc 'Transforms v1 data to v1.6'
task :"v1_to_v1.6" do
  total_start = Time.now

  Dir.mkdir(TEMP_PATH) unless File.exists?(TEMP_PATH)
  %w{ latin greek }.each do |lang|
    info("Processing #{lang}", true)

    dir = temp_dir(lang)
    Dir.mkdir(dir) unless File.exists?(dir)

    Dir.glob(xml_glob_at(v1_path(lang))) do |file|
      basename = File.basename(file)
      basename = basename.sub(/#{TB_EXTENSION}$/,'')
      basename = basename.sub(/#{XML_EXTENSION}$/,'')
      next if V1_TO_IGNORE.include?(basename)

      info("Transforming #{basename}")

      start = Time.now

      transformer = Treebank::Transform.new(File.read(file, :encoding => 'utf-8'))
      result   = transformer.transform

      filename = transformer.extract_cts_name(TB_EXTENSION) || basename
      stripped_filename = filename.sub(/#{TB_EXTENSION}/,'')
      if (basename =~ /#{stripped_filename}/)
        filename = basename
        filename << TB_EXTENSION
      else 
        filename = transformer.extract_cts_name(TB_EXTENSION) || basename
      end

      new_dir = v1six_path(lang)
      FileUtils.mkdir_p(new_dir) unless File.exists?(new_dir)
      File.open(File.join(new_dir, filename), 'w:UTF-8') do |f|
        f.write result
      end

      stop = Time.now
      time_elapsed = stop - start

      success("Transformed as #{filename} in #{time_elapsed.round(2)}s")
    end

    FileUtils.rm_rf(dir)
  end

  Dir.rmdir(TEMP_PATH)
  total_stop = Time.now
  total_time = total_stop - total_start

  success("Transformations completed in #{total_time.round(2)}s", true)
end
