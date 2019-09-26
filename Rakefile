namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end
  # Before we use migrate we should write the task below.
  # otherwise it'll not work because we need to connect files among them.

  task :environment do
    require_relative './config/environment'
  end

  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
  #the method above loads our dummy data for test.

  desc 'drop into the Pry console'
  task :console => :environment do
    Pry.start
  end
  #   We'll define a task that starts up the Pry console. We'll make this task
  # dependent on our `environment` task so that the `Student` class and the database
  # connection load first.
end


task :console do
end





namespace :greeting do
desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end
#if we want to write more than one task to rake,
#this is the way how we do it!
