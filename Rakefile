namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts 'hola de Rake!'
  end
end

namespace :db do
  desc 'migrate changes to the database'
  task :migrate => :environment do
    Student.drop_table
    Student.create_table
  end

  desc 'seeds the database with data'
  task :seed do
    require_relative 'db/seeds.rb'
  end
end

desc 'loads environment.rb'
task :environment do
  require_relative 'config/environment.rb'
end

desc 'drops into the Pry console'
task :console => :environment do
  Pry.start
end
