#THIS IS A PRACTICE TO SETUP AN IONIC APP DEV ENVIRONMENT AND START LEARNING APP DEV ON MULTIPLE DEVICES


Create the project
Now, we need to create a new Cordova project somewhere on the computer for the code for our app:

$ ionic start todo blank --type ionic1
That will create a folder called todo in the directory the command was run. Next, we will go into that directory and list the contents. Here is what the outer structure of your Ionic project will look like:

$ cd todo && ls

├── bower.json     // bower dependencies
├── config.xml     // cordova configuration
├── gulpfile.js    // gulp tasks
├── hooks          // custom cordova hooks to execute on specific commands
├── ionic.project  // ionic configuration
├── package.json   // node dependencies
├── platforms      // iOS/Android specific builds will reside here
├── plugins        // where your cordova/ionic plugins will be installed
├── scss           // scss code, which will output to www/css/
└── www            // application - JS code and libs, CSS, images, etc.
If you are planning on using any version control system, you can go ahead and set it up in this new folder.

Configure Platforms
Now, we need to tell ionic that we want to enable the iOS and Android platforms. Note: unless you are on MacOS, leave out the iOS platform:

$ ionic cordova platform add ios
$ ionic cordova platform add android
If you see errors here, make sure to follow the platform guides above to install necessary platform tools.


Test it out
Just to make sure the default project worked, try building and running the project (substitute ios for android to build for Android instead):

$ ionic cordova build ios
$ ionic cordova emulate ios
