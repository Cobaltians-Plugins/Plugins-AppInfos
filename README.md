# appInfos

appInfos plugin allows you to get some informations about the app, like its version number.


## How to use

* import the plugin to your project as explained [here](https://github.com/cobaltians/cobalt/wiki/Plugins-usage)
* Add the cobalt.appInfos.js to your web JS folder
* Add an html link to the cobalt.appInfos.js plugin script after the cobalt link in the HEAD tag

use the cobalt.getAppInfos shortcut like this

    //somewhere after cobalt inited
    cobalt.getAppInfos(function(infos){
        //You received device infos.
        cobalt.log('app version is :', infos.versionNumber)
    });

Current full returned fields are :

| field | type | description |
| ----- | ---- | ----------- |
| versionName | string     | the public verbose version number of the app. |
| versionCode | number     | the build number of the app (for app submissions). |
| deviceID | string     | a unique id you can use to identifiy this app user on this device (for push notifications or so) |
| lang | string     | the device current language. |


Sample : 

    {
        versionName : "1.5.2",
        versionCode : 4,
        deviceID : "645EAC64-[...]0F5",
        lang : 'en-US'
    }


## Planned features

 * appName ?
 * other ideas ? propose yours in the issues tracker
 * ...
