# sql-practice
Practice SQL using a docker image containing a jupyter notebook, pandas, and SQLAlchemy linked to preloaded MySQL databases

![SQLAlchemy](https://raw.githubusercontent.com/joseph-jnl/joseph-jnl.github.io/master/images/sql/jupyterSQL.png "SQLAlchemy")

## Install
### Step 1
Clone this repo:
``` 
git clone https://github.com/joseph-jnl/sql-practice.git
```

AND

Install [docker](https://www.docker.com/community-edition)

* [Ubuntu](https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/)
* [Mac](https://store.docker.com/editions/community/docker-ce-desktop-mac
)
* [Windows](https://store.docker.com/editions/community/docker-ce-desktop-windows)

(Note: For Linux Mint when adding the stable repo, '$(lsb_release -cs)' must be 
replaced with the ubuntu base, i.e. xenial)

### Step 2
Then build docker images:
``` 
sudo docker build -t josephjnl/jupyter-sql:latest \
https://github.com/joseph-jnl/sql-practice.git#master:images/jupyter-sql

sudo docker build -t josephjnl/mysql-practice:latest \
https://github.com/joseph-jnl/sql-practice.git#master:images/mysql-practice
```

OR download images:
``` 
sudo docker pull josephjnl/mysql-practice
sudo docker pull josephjnl/jupyter-sql
```

### Step 3
Start the mysql docker image (Only need to do this once unless you stop the container):
```
sudo docker run --name sqlpractice -itd --restart always --publish 3306:3306 --volume /srv/docker/mysql:/var/lib/mysql -d josephjnl/mysql-practice
```

Start the jupyter notebook docker image with:
(Note: Replace '/home/joe/work' with your own working directory to persist changes after
you stop the docker container)

Don't forget to include the /notebook from this repo in your working directory!
```
sudo docker run --name "jupyter-sql" -it --rm \
-p 8888:8888 -v /home/joe/work:/home/jovyan \
josephjnl/sql-practice:latest
```
Copy/paste the given URL into your browser to start the Juypter notebook

### Step 4
Open up one of the SQL practice jupyter notebooks found in the /notebook directory:

**Current notebooks**

* Lahman's Database - Baseball datebase containing tables such as player salaries, hitting, and pitching statistics.