# Mammoth Project Layout

[Draft 2/25/2014 11:08:25 PM] 

    www.example.com
    ├── configuration
    ├── functions
    ├── migrations
	│	├── development_example_migration.php
	│	├── development_example_migration.sql
	│	├── sql
    │       ├── full
    │       ├── up
    │           ├── 20111219100622_CreateButtonClickTable.sql 
	├── data
    ├── classes
    │   └── MammothExample
    │       ├── ContactController.php 
	│		├── System.php
    ├── environment
	│	├── development.php
	│	├── staging.php
	│	├── production.php
	│	├── local.php
	│	└── global.php
    ├── private
	│	├── js
	│	├── scss
    ├── public
	│	├── js
	│	│	└── default.js
	│	├── css
	│	│	└── default.css
	│	├── images
	│	├── fonts
	│	├── .htaccess
	│	├── index.php
	├── vendor
	│	└── (composer vendor directory)
	├── views
	│   ├── layouts
	│   ├── index.php
	│	├── contact.php
    ├── build.xml
    ├── include.php
    ├── compsoer.json
    ├── compsoer.lock
    ├── migrate.php
    ├── rotues.xml
    │  
    │  
    └──

## classes

### classes/MammothExample/System.php

This is the applications module configuration file. It loads any required routes, plugins, and other registries. For more information see the [module class](module-class) documentation.

## functions

Contains site specific global (or namespaced) functions definitions.

## migrations

Contains site specific schema/data migrations, and a running log of modules migrations.

[see: migrations]

### migrations/sql/up

Contains step by step migrations to bring the site specific SQL database up to date. 

### migrations/sql/full (optional)

Contains the definitions of all SQL tables in their latest current state. 
