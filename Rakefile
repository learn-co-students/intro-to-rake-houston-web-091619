require "pry"

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

desc 'prints out some dope shit'
task :lit do 
  puts 'ayy lmao'
end

desc 'start the mf console'
task :console => :environment do 
  Pry.start
end

desc 'does things in the environment'
task :environment do 
  require_relative './config/environment'
end

namespace :db do
  desc 'does stuff to the database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'puts mega seeds all the way up your butt'
  task :seed do 
    require_relative './db/seeds.rb'
  end

end
