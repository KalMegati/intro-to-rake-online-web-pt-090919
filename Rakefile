namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end
  
  desc 'pets the kitty'
  task :patto do
    puts "squish that cat!"
  end
end

namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end
  
  desc 'links to the environment file'
  task :environment do
    require_relative './config/environment'
  end
  
  desc 'seed the database with dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end