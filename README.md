# todo_symfony4
This is a simple Todo App with Symfony 4


# Installing Doctrine¶

First, install Doctrine support via the orm Symfony pack, as well as the MakerBundle, which will help generate some code:

 composer require symfony/orm-pack
 composer require --dev symfony/maker-bundle

# Configuring the Database¶

The database connection information is stored as an environment variable called DATABASE_URL. For development, you can find and customize this inside .en v:



# .env (or override DATABASE_URL in .env.local to avoid committing your changes)

# customize this line!
DATABASE_URL="mysql://db_user:db_password@127.0.0.1:3306/db_name"

to use sqlite:

DATABASE_URL="sqlite:///%kernel.project_dir%/var/app.db"


Now that your connection parameters are setup, Doctrine can create the db_name database for you:

 php bin/console doctrine:database:create

There are more options in config/packages/doctrine.yaml that you can configure, including your server_version (e.g. 5.7 if you're using MySQL 5.7), which may affect how Doctrine functions
