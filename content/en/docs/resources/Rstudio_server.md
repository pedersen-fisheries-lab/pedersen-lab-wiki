---
title: "Rstudio Server"
draft: false
images: []
menu:
  docs:
    parent: "resources"
weight: 100
toc: true
---

### Getting started with Rstudio in the cloud ☁️💻

RStudio Server enables you to provide a browser based interface to a version of R running on a remote Linux server.  
This allows you to work on complexe datasets/models without the worries of your computers own ressources.

Using Rstudio in the cloud also allows you to save your work in a safe environment without the worries of your laptop battery dying or your hard drive crashing.

Using Rstudio Server combined with git is a powerful way to streamline your work and test compute intensive mehtods before deplying to a High Performance Computing service such as [Compute Canada](https://ccdb.computecanada.ca/security/login)

#### Setting up a user (Admins only)

1.  Login to the server locally or via SSH
2.  Run the following code:

```console
#### 1. Get Rstudio Docker ID ####
sudo docker ps -a

#### 2. Open Container interactive shell ####
docker exec -it CONTAINER_ID /bin/bash

#### 3. Set new user login id ####
my_user=new_user

#### 4. Add the user ####
useradd ${my_user}
 
#### 5. Set the user password ####
passwd ${my_user}
 
#### 6. Create a home directory for the new user ####

mkdir /home/${my_user}
chown ${my_user}:${my_user} /home/${my_user}


#### 7. Close the shell ####
exit
```

3.  Finished
