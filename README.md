# SFDX  App
sfdx force:auth:web:login -r https://login.salesforce.com -a TP_reusablecomp_TP

## Dev, Build and Test

sfdx force:org:create -s -f config/project-scratch-def.json -a "TP_reusablecomp"

https://login.salesforce.com/packaging/installPackage.apexp?p0=04tB0000000M8Av

## TO BE TESTED
sfdx force:package:install --package 04tB0000000M8Av

## Resources

## DEPLOY TP
rd mdapioutput /S /Q
sfdx force:source:convert -d mdapioutput/
sfdx force:mdapi:deploy -d ./mdapioutput -c --testlevel RunLocalTests -u TrackerSIT -w 100


## Description of Files and Directories


## Issues


