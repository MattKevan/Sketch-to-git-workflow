# Sketch to Git workflow

This enables you to use Sketch as part of a true version-controlled workflow. If you’re a designer with development skills you’ll feel right at home.

It works by exporting a Sketch file into its constituent components whenever you hit save, mostly JSON files and images, so that it can be better uploaded to and managed by Git. Otherwise it'd just be a big blob of binary.

The script watches your project folder and exports your Sketch file whenever you hit save. When you pull any changes, a hook is fired to put all the bits back together again, incorporating your latest changes.

## Requirements

* Sketch 44+
* [Kactus](https://kactus.io)

## Installation

* Clone or download this repository.
* Rename it to that of your project.
* cd into your project folder.
* Run `npm install`.
* To create a new Sketch file, set your `filename` in the `package.json` to what you want to call it (default is `yourprojectname`). Then run `npm run new`.
* If you have an existing Sketch file, move it to the project folder and update `package.json` to match.

### Setup git

If you've cloned this repository, you should reinitialise your git repo.

* Create a new origin repository on Github/Bitbucket/Gitlab etc.
* Setup your git repo in your local project folder with `rm -rf .git && git init .`
* Add your new origin repository with `git add origin [...]`

## Usage

* cd into your project folder
* Run `npm start`
* Design, commit and push some new stuff.

### Pulling

Close your Sketch file before pulling any changes. It may confuse things if the file is still open.

### Cloning an existing project

If you run `npm start` in a freshly cloned project folder the script will fail as the Sketch file hasn't yet been reconstitued. You'll need to pull another commit from the repo to force the post-checkout hook to fire, or run the command manually with `npm run updateSketchFile`.

### Warning

Conflicts are a nightmare to sort out manually, so I'd recommend using the [Kactus](https://kactus.io) client for this as it has a nice visual inspector. There's no reason why, if you're using this script, you can't use the Kactus client as well as they both use the same tools under the hood.

## Acknowledgements

* [Kactus CLI](https://github.com/kactus-io/kactus-cli)
* [Kactus Git Workflow](https://github.com/thinkbright/kactus-git-workflow)
