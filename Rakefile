namespace :greeting do

  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outpts hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end
namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end
  task :environment do
    require_relative './config/environment'
  end

  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end

=begin
Describe feature:
1. Desc:
  Prints the words 'outputs hello to the terminal'
  desc is describing the method beneath itself

2. Do:
  everything to the left of the "do" statement
  is the condition.
  everything to the rieght and to the
  bottom is the code to execute.

3. task:
  performs a function with the name as a symbol
  
=end