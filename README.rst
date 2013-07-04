===================================
Mist.io on OpenShift using Buildout
===================================

This repository contains a buildout-based deployment template for mist.io.

It is based on https://github.com/kagesenshi/pyramid-buildout-openshift-quickstart by Izhar Firdaus.


Instructions
============

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

  https://mistio-<yourNamespace>.rhcloud.com

