#JsCat

JsCat is a ruby handler to load, concatenate and compress a directory of javascript files with the option to prioritize the load order of scripts (which is necessary for some js frameworks)

##Usage

    require File.join(File.dirname(__FILE__), '../src/JsCat')

    javascript = JsCat.new({
      :js_dir => 'scripts',             #read javascript files from this directory
      # :compress => 'true',            #uses/requires yui/compressor
      :prioritize => ['framework.js'],  #puts framework.js at the top of the file
      :ignore => ["script_c.js"],       #dont include these files 
      :output => "output/javascript.js" #write the file here
    })

    puts javascript.js