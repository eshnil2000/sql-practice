# sql-practice
Practice SQL using a docker image containing a jupyter notebook linked to a preloaded MySQL database

# Install
### Step 1
Install [docker](https://www.docker.com/community-edition)

Then build:
``` 
sudo docker build -t josephjnl/jupyter-sql:latest \
https://github.com/joseph-jnl/sql-practice.git#master:images/jupyter-sql

sudo docker build -t josephjnl/mysql-practice:latest \
https://github.com/joseph-jnl/sql-practice.git#master:images/mysql-practice
```

or download images:
``` 
sudo docker pull josephjnl/sql-practice