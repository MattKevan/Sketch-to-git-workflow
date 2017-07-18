# Kactus Git Workflow

This is a helper repository to use Sketch and `kactus-cli` as part of a true git workflow, no need for the Kactus app. If you’re a designer with development skills you’ll feel right at home.

## Requirements

* Sketch 44+
* [🌵 Kactus](https://github.com/kactus-io/kactus) (Only the Kactus Sketch plugin is required)

## Installation

* Run `npm install`
* Set your `filename` in the `package.json` config to match an existing sketch file (default is `yourprojectname`)
* Or use `npm run new` to create a new Sketch file based on `filename` in the `package.json`

### Setup git

If you've cloned this repository then you should reinitialise your git repo.

* Setup your git repo with `rm -rf .git && git init .`
* Add your origin repositry with `git add origin`

## Usage

* Run `npm start`
* Design, commit and push some new stuff
* ...
* Profit!

## About this project

We love the steps tools like Kactus and Abstract are taking to integrate design and development workflows. But as design and development nerds, we value the freedom to choose and manage our design workflow. We’re much faster with the command line instead of a seperate app and we don’t want to be tied by a specific online platform or git hosting service.

Kactus is a great step forward and the first time we can truly version control our Sketch files. This project aims to integrate a design workflow that mimics the development command line workflow we are used to. Watching files, auto reloading and automation where possible.

## Acknowledgements

[Kactus CLI](https://github.com/kactus-io/kactus-cli)