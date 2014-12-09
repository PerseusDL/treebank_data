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
#  Path Helpers  #
##################

TEMP_EXTENSION = ".tmp.xml"
TEMP_PATH = "temp_transformations"

def v1_path(lang)
  File.join('v1', lang, 'data')
end

def v1six_path(lang)
  File.join('v1.6', lang, 'data')
end

def xml_glob_at(path)
  File.join(path, '*.xml')
end

def temp_file(filename)
  stripped = File.basename(filename, '.xml')
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
  Dir.mkdir(TEMP_PATH) unless File.exists?(TEMP_PATH)
  %w{ latin greek }.each do |lang|
    info("Processing #{lang}", true)

    dir = temp_dir(lang)
    Dir.mkdir(dir) unless File.exists?(dir)

    Dir.glob(xml_glob_at(v1_path(lang))) do |file|
      basename = File.basename(file)
      info("Transforming #{basename}")

      start = Time.now

      transformer = Treebank::Transform.new(File.read(file))
      result   = transformer.transform
      filename = transformer.extract_cts_name('.xml')

      new_dir = v1six_path(lang)
      FileUtils.mkdir_p(new_dir) unless File.exists?(new_dir)
      File.write(File.join(new_dir, filename), result)

      stop = Time.now
      time_elapsed = stop - start

      success("Transformed as #{filename} in #{time_elapsed.round(2)}s")
    end

    system("rm -rf #{dir}")
  end
  Dir.rmdir(TEMP_PATH)
end
