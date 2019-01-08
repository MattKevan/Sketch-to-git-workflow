# Sketch Git Workflow

This is a helper repository to use Sketch as part of a true git version control workflow. If you’re a designer with development skills you’ll feel right at home.

The script works by decomposing a Sketch file into its constituent components, mostly JSON files and images, so that it can be better uploaded to and managed by Git. Otherwise it'd just be a big binary blob. This happens automatically whenever the Sketch file you're working on is saved. When you pull any changes, a hook is run to reconstitute all the bits back to a Sketch-readable file.

## Requirements

* Sketch 44+
* [Kactus](https://kactus.io)

## Installation

* Clone or download this repository
* cd into your project folder
* Run `npm install`.
* To create a new Sketch file, set your `filename` in the `package.json` to what you want to call it (default is `yourprojectname`). Then run `npm run new`.
* If you have an existing Sketch file, move it to the project folder and update `package.json` to match.

### Setup git

If you've cloned this repository, you should reinitialise your git repo.

* Create a new origin repository on Github/Bitbucket/Gitlab etc.
* Setup your git repo in your local project folder with `rm -rf .git && git init .`
* Add your new origin repository with `git add origin [...]`

## Usage

### Committing and pushing

* cd into your project folder
* Run `npm start`
* Design, commit and push some new stuff.

### Cloning

If you run `npm start` in a freshly cloned project folder the script will fail as the Sketch file hasn't been reconstitued yet. You'll need to pull another change from the repo to force the post-checkout hook to run, or run the command manually with `npm run updateSketchFile`.

### Warning

Conflicts are a nightmare to sort out manually, so I'd recommend using the [Kactus](https://kactus.io) client for this as it has a nice visual inspector. There's no reason why, if you're using this script, you can't also use the Kactus client.

## About this project

This project is a modified version of Thinkshout's Kactus Git Workflow, improving the documentation. 

## Acknowledgements

* [Kactus CLI](https://github.com/kactus-io/kactus-cli)
* [Kactus Git Workflow](https://github.com/thinkbright/kactus-git-workflow)
