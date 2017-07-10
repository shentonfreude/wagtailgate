=============================
 Git clone and fork upstream
=============================

Fork then clone a project, set the upstream on master to the original,
work on a local feature/bug branch, then submit pull request.

Good info:

https://egghead.io/lessons/javascript-how-to-fork-and-clone-a-github-repository

Get local copy and set master to upstream
=========================================

Fork the project on the github page: icon on top right; select our username.

Clone or download: copy the SSH URL. This creates a copy in github as
USERNAME/REPONAME.git.

Copy SSH-URL from our fork, move into it::

  git clone SSH-URL
  cd REPONAME

Sync our copy with upstream's (original) 'master' repo. Go to original
project and get original ORIGINAL-URL::

 git remote add upstream ORIGINAL-URL

Config local fork to get info about original upstream remote::

 git fetch upstream

Set our master to track upstream's master::

  git branch --set-upstream-to=upstream/master master

Develop
=======

Create new branch.

Figure out how to set up the development environment. Maybe::

  npm install

Run the tests to make sure they work as is.

  npm t
  npm build

Config the local repo to push our changes to and push it::

  git push --set-upstream origin/BRANCHNAME


Submit to Upstream
==================


Go to original upstream github page. You may see your fork listed as a new item. Hit Create new Pull Request. Set the base branch to the one you're working from (e.g., master, 1.6.4, ...) and ensure your head fork and branch are correct.
