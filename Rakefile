require "bundler/gem_tasks"

task default: :prepare

task :prepare do
  cd "ext/libsass"
  # sh "echo 'task goes here' | cat - Makefile > temp && mv temp Makefile"
  sh "make lib/libsass.so"
end

task :test do
  $LOAD_PATH.unshift('lib', 'test')
  Dir.glob('./test/**/*_test.rb') { |f| require f }
end
