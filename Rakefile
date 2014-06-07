require 'pathname'
require 'github/markdown'

task :build do
  base   = Pathname.new(__FILE__).dirname
  build  = base.join 'build'
  readme = base.join('README.md').read
  html   = GitHub::Markdown.render readme

  build.mkpath unless build.directory

  build.join('index.html').open('w') do |file|
    file.write html
  end

  puts "Saved as build/index.html"
end

task :open => [:build] do
  base = Pathname(__FILE__).dirname
  `google-chrome #{base.join('build', 'index.html').to_s}`
end
