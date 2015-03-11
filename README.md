Installing Drupal Using Composer Create-Project
===

What?
---

This repo is a test of whether you can use Composer's create-project command to install a useful Drupal 8 installation.

It uses github and travis-ci to build a Drupal installation and then try to run tests.

We are limiting the tests to PHPUnit and some Entity module tests, because otherwise travis will time out on us.

Why?
---

Some folks think you can use create-project to install Drupal. Others don't. Let's find out what Drupal's actual behavior is.

What does this test show?
---

This test shows whether Drupal is modular enough to run PHPUnit tests from the command line and some SimpleTest tests, after using composer to install it.
