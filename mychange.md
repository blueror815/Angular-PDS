# clinic-app

This repo serves as the hybrid mobile/desktop version of the clinic application.


# Technology used

The app uses cordova to build the hybrid applications with a foundation template from [this theme](https://wrapbootstrap.com/theme/beadmin-bootstrap-admin-theme-WB020NMN7).
This application utilizes Angular.js and a number of js libraries that can be found in the project inside the vendor directory.

# First Run
Once you have the repo cloned, navigate to /master and run `npm install`, then `bower install`.  
This will setup the proper node modules and dependencies.

All .scss and js files are compiled to the /www directory where a local server can be run to view the app locally.
To compile and watch files, simply run `gulp` from the /master directory AFTER all dependencies have been installed.

Next make sure you have the latest cordova cli tools by running `npm install -g cordova`.  

Next you may need to add platforms to run, do this with the command `cordova platform add browser/ios/android`
The cordova docs are [here](https://cordova.apache.org/docs/en/latest/guide/overview/).

You should finally be ready to run the app! cd to the root directory and run `cordova run [platform`]  This is usually
ios or android.  This command will spin up an emulator, or browser depending on the platform chosen.
Alternatively, you can run a server from the /www directory to view the app in a local browser.  A common convention is
to run `python -m SimpleHTTPServer` from /www.

# Environments
There are two default ways to build the app now using gulp. Running the default task from /master ie., `gulp` will
set the api url to the 'local' definition in /master/configFile.json.  Running `gulp build` will switch the api to
the PROD url as well as concat and minify all assets.

#Next Steps
As development continues, I'll do my best to keep this doc updated as well add more tasks to gulp including environment
variables and running multiple servers without having to open a separate terminal window.

