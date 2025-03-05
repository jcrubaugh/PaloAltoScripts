# PaloAltoScripts
Scripts I use to automate migration of data between different palo alto clusters

If your going to be using this repo, you will want to ensure that you have the following variables set in your windows environment

Set-EnvironmentVariable -Name panoramapikey -Value 'yourapikey' -StoreName User


Set-EnvironmentVariable -Name panoramanpapikey -Value 'yourapikey' -StoreName User


Set-EnvironmentVariable -Name panoramaprodapikey -Value 'yourapikey' -StoreName User


** Note the name above here are my names of the key files where i host the variables  your names can be different, just remember whatever name you use matches the key file name.


if your on a mac you would need to do:
follow steps in this article to add  an environmental variable https://yngstone89.medium.com/setting-up-environment-variables-in-mac-os-28e5941c771c  or a similar artice. 

 ##notes on differences between URL in the url.py files ####
 
 the version is specific in the api calls is the version of the base software when the panorama was built, just because you upgraded to 
 version 10 or 11 or even a sub version 10.2 or 11.1 the api doesnt seem to match. so you may neeed to play with the version if you don't 
 know what the base version is. sometimes you can put /latest/ in there or someetimes you might just be able to leave it off. Generally 
 if you want to know the base version you can check in aws and see what image was used and that version "should" work in your api calls

 some of these scripts have been overly manipulated because between 10.1 and 10.2 some of the format for posting has changes... once we are moving same version to version, 
 some of the customiztion will be able to be removed because the source format and destination format of the data will be the same.
