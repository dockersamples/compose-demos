# Using Secrets with Docker Compose


To create the secret files for your Docker Compose services, you can use the following steps:

## Create Secret Files:

Start by creating text files that contain the secrets you want to use. You can use a text editor or command-line tools to create these files.

For example, to create db_password.txt and db_root_password.txt files with sample secrets, you can use a text editor or the echo command in a terminal:


```
## Create db_password.txt with a secret password
echo "your_db_password_here" > db_password.txt
```

## Create db_root_password.txt with a secret root password

```
echo "your_db_root_password_here" > db_root_password.txt
```

Replace "your_db_password_here" and "your_db_root_password_here" with the actual passwords you want to use.

## Place the Secret Files:

Place the created secret files in the same directory as your docker-compose.yml file or any directory where you plan to run your Docker Compose stack. The paths in your docker-compose.yml file should be relative to the location where you store these files.

## Bring up the app

```
docker compose up -d -build
```

