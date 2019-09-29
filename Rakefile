
namespace :greeting do
desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

desc 'outputs hola to terminal'
  task :hola do
    puts 'hola de Rake!'
  end
end

desc 'access to the environment file'
task :environment do 
require_relative './config/environment'
end


namespace :db do

  
  desc 'migrate changes to the database'
    task :migrate => :environment do
      Student.create_table
    end

  desc 'seed the database with some dummy data'
    task :seed do
      require_relative './db/seeds.rb'
   end
  
 
end 

desc 'pry console for testing'
task :console => :environment do
  Pry.start
end