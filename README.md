Private Dropbox .NET SDK
========================

This repository is used to generate the [public Dropbox .NET SDK]
(https://github.com/dropbox/dropbox-sdk-dotnet).

This repository contains no auto-generated code.

Basic Setup
-----------

1. Clone the public and private SDK repo into `~/src`.

2. In the private SDK repo, run `git submodule update` to pull in the `spec`
   and `babel` sub repos.

Updating the SDK for a new spec
-------------------------------

1. Go into the `spec` folder and update it to the desired commit. To update to
   the latest, simply use:

    $ git pull

2. Commit the change of the sub repo to the private SDK repo. Do not do this
   from a sub repo folder:

    $ git commit -a -m "Updated spec"
    $ git push

3. Use the `generate.py` script with the path to the local check out of the public:

    $ python generate.py -h
    $ python generate.py ../dropbox-sdk-dotnet

4. From the public repo, open up the `Dropbox.Api.sln` in Visual Studio and run
   the included examples as a sanity check.

5. Commit and push the public repo.


Publishing a new SDK
--------------------

From the private repo, run `buildall.cmd`. TBD.


Generating Docs
---------------

We use GitHub pages. TBD.

