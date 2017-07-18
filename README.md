This is a helper repository to use Sketch and `kactus-cli` as part of a true git workflow, no need for the Kactus app. If you’re a designer with development skills you’ll feel right at home.

# Installation

* Run `npm install`
* Set your `filename` in the `package.json` config to match an existing sketch file (default is `yourprojectname`)
* Or use `npm run new` to create a new Sketch file based on `filename` in the `package.json`

**Setup git**

If you've cloned this repository then you should reinitialise your git repo.

* Setup your git repo with `rm -rf .git && git init .`
* Add your origin repositry with `git add origin`

# Usage

* Run `npm start`
* Design, commit and push some new stuff
* ...
* Profit!

# Known limitations

* After merging changes the Sketch file needs to be closed and reopened to see the changes applied in Sketch.

# About this repository

We love the steps tools like Kactus and Abstract are taking to integrate design and development workflows. But as design and development nerds, we don't like arbritary limitations in the form of having to use yet another platform or being forced to use a certain service. We are used to using git in the command line and we would like to use the workflow we're accustomed to for design projects.

# Acknowledgements

[Kactus CLI](https://github.com/kactus-io/kactus-cli)