SONIC OPEN KANG PROJECT
===================

SONIC OPEN KANG PROJECT platform manifest


Getting Started
---------------
To get started with the SONIC OPEN KANG PROJECT sources, you'll need to get
familiar with [Git and Repo](http://source.android.com/source/version-control.html).


Create the Directories
----------------------

You will need to set up some directories in your build environment.

To create them run:

    mkdir -p ~/bin
    mkdir -p ~/SOKP


Install the Repository
----------------------

Enter the following to download the "repo" binary and make it executable:

curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo && chmod a+x ~/bin/repo

You may need to reboot for these changes to take effect. 
Now enter the following to initialize the repository:

    cd ~/SOKP


Repositories:
---------------

Before you continue --> run this in the terminal
----------------------------------------
    repo init -u git://github.com/SOKP/platform_manifest.git -b sokp-443 
    
    && 
    
    repo sync -f

*PLEASE NOTE THAT YOU MUST USE THE -f flag when repo syncing/initializing if you want to sync with our default -j4 setup as android.googlesource seems to like to reject your requests if you set your -jflag too high. 
if you wish to avoid this issue run it repo sync -j1 otherwise -f (force) is recommended so it will resync the repos it gets error codes on. Thank you and have a nice day.*


Building the System
---------------

Initialize the environment with the envsetup.sh script. Note that replacing "source" with a single dot saves a few characters, and the short form is more commonly used in documentation.

    . build/envsetup.sh
    brunch n7100 ( Replace n7100 with your device name if you are building for other devices )

You can also build (and see how long it took) for specific devices like this:

Build the Code:

    . build/envsetup.sh
    time brunch n7100 ( Replace n7100 with your device name if you are building for other devices )


Submitting Patches
------------------
Updated Soon

Git TrickMarks
------------------
Creating a git branch with no ancestry git checkout --orphan git rm --cached $(git ls-files) git add NOTICE git commit -m "dummy commit" Then u push the goodies ;)

If you have any issues/questions please contact us in email id : audiogod@live.com If you need any live help contact us in hangouts id : audiogod@live.com
