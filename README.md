# redmine_nginx
redmine+mysql+nginx

1. To start a stack type the command "docker-compose -f redmine_stack.yml up -d"
2. To stop a stack type the command "docker-compose -f redmine_stack.yml down"
3. The "certs" directory contains ssl certificates.
4. The "data" directory is used for store Redmine data.
5. The "mysql_data" directory is used for store MySQL data.
6. The mysql_pass file contains MySQL root password. 
7. The redmine_pass file contains password for access to MySQL server(for root user by default).
8. After the stack is running, you can use the application at https://localhost.
9. For backup redmine database run command - mysqldump --user=<USERNAME> --password=<PASSWORD> --skip-extended-insert redmine > redmine.sql
10. For restore redmine database run command - mysql --user=<USERNAME> --password=<PASSWORD> redmine < redmine.sql
11. For migration to new version of database run command - "rake db:migrate RAILS_ENV=production" in redmine root directory, for this image this is /usr/src/redmine
12. For installation plugins put them into /usr/src/redmine/plugins dirrectory and set correct owner(redmine:redmine) 
