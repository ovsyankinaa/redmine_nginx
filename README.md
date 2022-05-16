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

