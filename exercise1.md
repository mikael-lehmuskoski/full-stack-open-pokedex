
# Exercise 11.1

The following text will review CI-related considerations as they relate with the following scenario:

 - a project using Python
 - team of 6 devs
 - release date approaching at terminal velocity

## common steps in CI

  ### linting

  Linting is an important part of working as a team and making sure the product is maintainable. 
  There are several linting tools available for Python. 
  Next is a quick rundown of three of the most popular linting tools for Python: 

    - pylint
      - pylint is the most popular linter made for Python
      - highly customizable and is easily integrated into popular CI-services
    - flake8
      - flake8 is a linter aggregator meaning it makes use of several tools for different tasks
    - mypy
      - mypy is a very popular Python linter authored by Jukka Lehtosalo 

  All of the previously mentioned linters are also available locally in VSCode via the Python plugin.

  ### build

  Python is an interpreted language. As such it requires no build step in the pipeline.

  ### testing

  Frequent testing makes sure that things don't break silently, without the devs knowing about it. 

  There are two main types of testing: unit tests and integration tests. 
  Unit tests focus on a specific piece of code while integration testing makes sure all the different pieces of code function together. 

  There are several test runners used with Python. All of them can be integrated into several CI-services.

  test runners: 
    - unittest
    - nose or nose2
    - pytest

  Again, the test runners listed above are also included in the VSCode Python plugin.

## CI services

  Alternatives to Jenkins and Github Actions include:
  - Gitlab CI
  - Travis CI
  - AWS CodePipeline

## self-hosted vs cloud-based

  Since the project uses Python and the team is relatively small, it would make more sense to use a cloud-based CI service. 
  If there was a resource-intensive build step in the pipeline and/or more developers in the team, a self-hosted CI server might make more sense.