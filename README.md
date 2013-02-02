labtech_script_java_7_update_13
==============================================

Script and files to install Java 7 Update 13

REQUIREMENT: Caching must be setup

Will update 32 and 64 bit

Script does the following:
* Exits script if Windows Server
* Verifies that Java 7 Update 13 is not already installed
* Checks EDF [Disable Java Updates - Computers>Exclusions tab]
    If box is checked a ticket is created and script is exited
* Creates Java folder in cache directory
* Downloads Java Uninstall batch file from LTShare to cache directory
* Downloads Java Install files from LTShare to cache directory
* If files cant be downloaded a ticket is opened and the script is exited
* Any open browsers are killed (Internet Explore, Firefox, Chrome, Opera)
* Any old version of Java is uninstalled (javaremove.bat)
* Java 7 Update 13 is installed
* Java Update scheduler is killed
* Java Update Scheduler and AutoUpdate are removed from registry
* Software list is resent to verify install
    If install is not successful then a ticket is opened and script is exited
    If install is successful then a ticket is opened and script is exited

NOTES:
==========

I am not affiliated with Labtech Software. Please use these at your own risk. 

If you have any additions or better ways to do this please hit me up on [IRC](http://webchat.freenode.net/?nick=reddit_user_.&channels=%23%23labtech&uio=d4), my nick is cgauss.