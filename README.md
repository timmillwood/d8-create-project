Installing Drupal Using Composer Create-Project
===

Status
---
[![Build Status](https://travis-ci.org/paul-m/d8-create-project.svg?branch=master)](https://travis-ci.org/paul-m/d8-create-project)

What?
---

This repo is a test of whether you can use Composer's create-project command to install a useful Drupal 8 installation.

It uses github and travis-ci to build a Drupal installation and then try to run tests.

We are limiting the tests to PHPUnit and one entity test, because otherwise travis will time out on us.

We are emulating this sequence of commands in travis-ci:

    $ composer create-project drupal/drupal drupal 8.0.*@dev
    $ cd drupal
    $ ./vendor/bin/phpunit -c core/
    $ php ./core/scripts/run-tests.sh [more stuff] --class 'Drupal\system\Tests\Entity\EntityFieldTest'

How?
---

The travis-ci build happens whenever someone pushes to this repo. If you don't have access, you can't push against this repo (and you don't). You can, however, choose from the following options:

* Fork your own repo, and push to your own repo to your heart's content.
* Perform the test locally. Just perform the commands listed in the What? section.

Why?
---

Some folks think you can use create-project to install Drupal. Others don't. Let's find out what Drupal's actual behavior is.

What does this test show?
---

This test shows whether Drupal is modular enough to run PHPUnit tests from the command line and some SimpleTest tests, after using composer to install it.
