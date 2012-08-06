Make your GlassFish3 running on OpenShift
============================

This git repository helps you get up and running quickly w/ a GlassFish3 installation on OpenShift.

NOTE: admin console of GlassFish is disabled in this sampel app.

Create a DIY app on OpenShift
----------------------------

Create an account at http://openshift.redhat.com/ , don't forget to create a namespace and install client tools as well.

Create a python application

    rhc app create -a glassfish -t diy-0.1

Grab this quickstart codes and make it working for you!

    cd glassfish
    git remote add upstream -m master git://github.com/lulinqing/openshift-glassfish3-sample.git
    git pull -s recursive -X theirs upstream master
    git push

That's it, you can now checkout your GlassFish3 at:

    http://glassfish-$yournamespace.rhcloud.com

And a sample war has been deployed already:

    http://glassfish-$yournamespace.rhcloud.com/openshift
