$LOAD_PATH.unshift File.dirname(__FILE__)
require 'rake'
require 'guard/guard'

# load the "build" rake tesk
Rake.application.init
Rake.application.load_rakefile

module ::Guard
  class CustomCSS < ::Guard::Guard
    def run_all
    end

    def run_on_changes(paths)
      puts "Building Custom.css"
      Rake.application[:build].invoke
    end
  end
end

guard 'customcss' do
  watch(%r{main.scss$})
  watch(%r{stylesheets\/.+\.scss$})
end
