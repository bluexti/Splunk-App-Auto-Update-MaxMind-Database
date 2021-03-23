# Splunk-App-Auto-Update-MaxMind-Database
Splunk App that auto updates the max-mind database (used for iplocation command)

### Download from Splunkbase
TODO


OVERVIEW
--------
The Splunk app auto updates MaxMind database under $SPLUNK_HOME$/share/. This is automation of steps mentioned here - https://docs.splunk.com/Documentation/Splunk/8.1.3/SearchReference/Iplocation#Updating_the_MMDB_file


* Author - CrossRealms International Inc. (Vatsal Jagani)
* Version - 1.0.0
* Build - 1
* Creates Index - False
* Compatible with:
   * Splunk Enterprise version: 8.0, 7.3, 7.2 and 7.1
   * OS: Platform independent
   * Browser: Google Chrome, Mozilla Firefox, Safari



TOPOLOGY AND SETTING UP SPLUNK ENVIRONMENT
------------------------------------------
This app can be set up in two ways: 
  1. Standalone Mode: 
     * Install the `Auto Update MaxMind Database`.
     * App setup is required.
  2. Distributed Mode: 
     * Install the `Auto Update MaxMind Database` only on the search head.
     * App setup is required on SH.
     * App installation is not required on any other instance.


INSTALLATION
------------
Follow the below-listed steps to install an App from the bundle:

* Download the App package.
* From the UI navigate to `Apps > Manage Apps`.
* In the top right corner select `Install app from file`.
* Select `Choose File` and select the App package.
* Select `Upload` and follow the prompts.



CONFIGURATION
-------------
* Open the App and perform the configuration.
* The complete details about configuration is present on the dashboard directly.


UNINSTALL APP
-------------
To uninstall app, user can follow below steps:
* SSH to the Splunk instance
* Go to folder apps($SPLUNK_HOME/etc/apps)
* Remove the `maxmind_auto_update_splunk_app` folder from apps directory
* Restart Splunk

KNOWN LIMITATION
----------------
* NA

RELEASE NOTES
-------------
Version 1.0.0 (March 2021)
* App created based on URL from March 2021 on MaxMind to download the database.


OPEN SOURCE COMPONENTS AND LICENSES
------------------------------
* NA


TROUBLESHOOTING
---------------
* Confirm that the database has been updated:
  * Run `| updatemmdbfile` search to update the database manually.
  * Go to the location of MaxMind database (default: /opt/splunk/share/GeoLite2-City.mmdb file) and see if the last modified time for the file is recent.


CONTRIBUTORS
------------
* Vatsal Jagani
* Preston Carter


SUPPORT
-------
* Contact - CrossRealms International Inc.
  * US: +1-312-2784445
* License Agreement - https://d38o4gzaohghws.cloudfront.net/static/misc/eula.html
* Copyright - Copyright Crossrealms Internationals, 2020