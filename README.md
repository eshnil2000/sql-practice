# sql-practice
Practice SQL using a docker image containing a jupyter notebook linked to a preloaded MySQL database

# Install
### Step 1
Install [docker](https://www.docker.com/community-edition)

Then build:
``` 
sudo docker build -t josephjnl/sql-practice:latest \
https://github.com/joseph-jnl/sql-practice.git#master:image
```

or download image:
``` 
sudo docker pull josephjnl/sql-practice