require 'pry'
#require 'sinatra/activerecord/rake'

task :environment do 
  require_relative './config/environment'
end

desc 'outputs hello to the terminal'
  namespace :greeting do
    task :hello do
      puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

desc 'drop into the Pry console'
  task :console => :environment do
    Pry.start
  end

namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
  end
end

namespace :db do
  desc 'seed the database with some dummy data'
  task :seed do
   require_relative './db/seeds.rb'
  end
end

# desc "start our app console"
# task :console do
#   ActiveRecord ::Base.logger = Logger.new(STDOUT)
#   Pry.start
# end