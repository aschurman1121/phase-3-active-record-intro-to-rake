
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



namespace :db do
  desc 'migrate changes to your database'
  task migrate: :environment do
      #task above creates a task dependency -
      # -tells rake to run environment before migrate
      # the code we are running needs access to the environment file
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task seed: :environment do
    require_relative './db/seeds'
  end

end

task :environment do
  require_relative './config/environment'
end
# require_relative is used to refer to files within the directory, it is aware of the entire directory

desc 'drop into Pry console'
task console: :environment do
  Pry.start
end

