namespace :assets do
  desc 'Precompile assets'
  task :precompile do
    sh "bundle exec sass --update _scss:css --style compressed"
    sh "bundle exec jekyll"
  end
  task :devcompile do
    sh "bundle exec sass --update _scss:css --debug-info"
    sh "bundle exec jekyll"
  end
  task :autocompile do
    sh "bundle exec sass --watch _scss:css --debug-info"
    sh "bundle exec jekyll serve"
  end
end

task :default => ["assets:precompile"]
task :dev => ["assets:devcompile"]
task :watch => ["assets:autocompile"]