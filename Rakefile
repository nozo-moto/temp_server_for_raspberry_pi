task :default => [:start]

task :init do
  system "bundle install --path vendor/bundle --without production"
end

task :test do
  Dir.glob('./test/*_test.rb').each { |test_file|
    system "bundle exec ruby #{test_file}"
  }
end

task :start do
  system "bundle exec rackup -o 0.0.0.0"
end
