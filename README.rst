===================================
Mist.io on OpenShift using Buildout
===================================

This repository contains a buildout-based deployment template for mist.io

Running on OpenShift
=====================

Create an account at http://openshift.redhat.com/

Create a DIY application::
  
  rhc app create -a mistio -t python-2.6

Add this upstream repo::
  
  cd mistio
  git remote add upstream -m master git@github.com:mistio/mist.io-openshift
  git pull -s recursive -X theirs upstream master

Then push the repo to OpenShift (this will take quite a while to finish)::
  
  git push

Thats it, you now can check out your application at::

  http://mistio-$yournamespace.rhcloud.com
