namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc'outputs hello to the terminal, en espanol'
  task :hola do
    puts "hola de Rake!"
  end
end

desc 'begins console session'
task :console do
  Pry.start
end

task :environment do
  require_relative './config/environment'
end

namespace :db do
  desc 'migrate data to the database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end
