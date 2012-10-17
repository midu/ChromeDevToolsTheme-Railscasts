require 'rubygems'
require 'sass'

task default: [:build]

desc 'builds Custom.css'
task :build do
  path = File.expand_path './main.scss'
  Sass.compile_file path, 'Custom.css'
end
