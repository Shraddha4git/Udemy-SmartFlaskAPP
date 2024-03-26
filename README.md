## Overview

# SSH Testing
node {
  sshagent (['docker-log-ubuntu-keys']) {
    sh 'ssh -o StrictHostKeyChecking=no -l ubuntu 52.66.118.7 who'
  }
}

node {
  sshagent (['docker-log-ubuntu-keys']) {
    sh 'ssh -o StrictHostKeyChecking=no -l ubuntu 52.66.118.7 uname -a'
  }
}

## Key Python Modules Used
- Flask: micro-framework for web application development
- SQLAlchemy - ORM (Object Relational Mapper)
- Flask-Bcrypt - password hashing
- Flask-Login - support for user management
- Flask-WTF - simplifies forms

This application is written using Python 3.10.

## Running the application
DirPath/SmartFlaskAPP>python run.py

## Unit Testing and Code Coverage
Use pytest to execute unit-tests
pytest --cov=main --junitxml=./xmlReport/output.xml
python -m coverage xml

### Notes:
SQLlite DB in instance folder
If you clean the whole DB, you'll need to register a user first to login.
