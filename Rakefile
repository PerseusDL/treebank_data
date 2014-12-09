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

def v1_path(lang)
  File.join('v1', lang, 'data')
end

def xml_glob_at(path)
  File.join(path, '*.xml')
end

###########
#  Tasks  #
###########

desc 'Transforms v1 data to v1.6'
task :"v1_to_v1.6" do
  %w{ latin greek }.each do |lang|
    info("Processing #{lang}", true)

    Dir.glob(xml_glob_at(v1_path(lang))) do |file|
      basename = File.basename(file)
      info("Transforming #{basename}")
    end
  end
end
