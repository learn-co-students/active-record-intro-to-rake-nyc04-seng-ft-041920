namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola de Rake'
  task :hola do
    puts "hola de Rake!"
  end
end

task :environment do
  require_relative './config/environment.rb'
end
desc 'drop into pry'
task :console => :environment do
  pry.start
end

namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed database with dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end
