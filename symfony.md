# **Symfony command**

## **install symfony composer**

### create project composer <= v3.4

`> composer create-project symfony/framework-standard-edition my_project_name "3.4.*"`

### create project composer v^3.4

#### run this if you are building a microservice, console application or API

- `> composer create-project symfony/skeleton:"^5.3" my_project_directory`

#### run this if you are building a traditional web application

- `> composer create-project symfony/skeleton:"^5.3" my_project_directory`
- `> cd my_project_directory`
- `> composer require webapp`

## **install symfony-cli(windows)**

#### open powershell

#### install scoop

- `> Set-ExecutionPolicy RemoteSigned -Scope CurrentUser # Optional: Needed to run a remote script the first time`
- `> irm get.scoop.sh | iex`

#### install symfony-cli

`> scoop install symfony-cli`

### create new symfony project

`> symfony new my_project_directory --version=5.3 --webapp`

#### The `> --webapp` parameter: building traditional web application

## **php bin/console**

### start server

`> php bin/console server:run`

### autoload: psr4: '':src/

`> composer dump-autoload`

### add config.yml

`templating: engines: ['twig']`

### create bundle

`> php bin/console generate:bundle]`
