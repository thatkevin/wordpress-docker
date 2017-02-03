# wordpress-docker
Pop your theme in here, whack in an SQL dump, bobs yr uncle. This is just for dev on a WP site, not for production.

# set up
Create an .env file in the root with the following:

    WORDPRESS_DB_PASSWORD=xxx
    WP_ADMIN_USER=xxx@exampkle.com
    WP_ADMIN_USER_PASS_HASH=$1.xxxx.xxx.xx
    MYSQL_ROOT_PWD=xXxXxXxX

Generate the hash, dont just send a password over.

# migrating 
Put your existing Wordpress SQL in the "seed" folder, as either an .sql or tar.gz file - this will be added to the database. You should set your root URLs as '/'

# themes
Put them within the correctly named subfolders in the 'theme' folder

# usage
Install docker compose, and run docker-compose from the root. Visit the IP given by the dump in your browser.

# troubleshooting
Wordpress may require you go to /wp-admin and upgrade the database.
