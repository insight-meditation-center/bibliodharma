require 'colorize'

desc 'Dump the local DB to the ./db/seed-db.sql file.'
task :dump_db do |t|
  exec_command('docker-compose exec mysql sh -c "exec mysqldump --all-databases -uroot -ppassword" > db/seed-db.sql')
end

def exec_command(cmd)
  puts "  #{cmd}".green
  puts `#{cmd}`.split("\n").map {|l| "  #{l}"}.join("\n")
end
