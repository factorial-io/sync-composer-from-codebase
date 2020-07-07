# Sync composer from an existing code base

## Prerequisites

1. You need PHP 7.2 on your local
2. You need at least one drupal 7 installation where composer.json is not in sync with the installed modules. The installed modules should be committed to the git repo.

## Installation

1. Clone this repository to a place suitable for you
2. cd into that folder
3. run `composer install`
4. run `chmod +x bin/scfc`


## Usage

1. cd into the drupal 7 installation.
2. Make sure your project is clean, no modified files, `git status` does not show anything.
3. Run the tool via `/bla/myfolder/bin/scfc update .`
4. check the diff of `composer.json`
5. try to run `composer update --lock`
6. if this fails, delete `composer.lock` and run `composer install`
7. Check the output of `git status` and `git diff`
