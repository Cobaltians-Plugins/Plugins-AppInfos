#appInfos

appInfos plugin allows you to get some informations about the app, like its version number.


##How to use

* import the plugin to your project as explained [here](https://github.com/cobaltians/cobalt/wiki/Plugins-usage)
* Add the cobalt.appInfos.js to your web JS folder
* Add an html link to the cobalt.appInfos.js plugin script after the cobalt link in the HEAD tag

use the cobalt.getAppInfos shortcut like this

    //somewhere after cobalt inited
    cobalt.getAppInfos(function(infos){
        //You received infos. It contains 'versionCode', 'versionNumber', and so on.
        cobalt.log('app version is :', infos.versionNumber)
    });

Current full returned object is :

    {
        versionName : "1.5.2" //the public verbose version number of the app.
        versionCode : 4, //the build number of the app (for app submissions)
        deviceID : "645EAC64-[...]0F5", // a unique id you can use to identifiy this app user on this device (for push notifications or so
        lang : 'en-US' // the device current language
    }


##Planned features

 * appName ?
 * other ideas ? propose yours in the issues tracker
 * ...
