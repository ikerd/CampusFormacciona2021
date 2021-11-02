Moodle App
=================

This is the primary repository of source code for the official mobile app for Moodle.

* [User documentation](https://docs.moodle.org/en/Moodle_app)
* [Developer documentation](http://docs.moodle.org/dev/Moodle_App)
* [Development environment setup](https://docs.moodle.org/dev/Setting_up_your_development_environment_for_the_Moodle_App)
* [Bug Tracker](https://tracker.moodle.org/browse/MOBILE)
* [Release Notes](https://docs.moodle.org/dev/Moodle_App_Release_Notes)

License
-------

[Apache 2.0](http://www.apache.org/licenses/LICENSE-2.0)


Binuc: Formacciona
==================

Versión de node y npm necesarias (Para la versión 3.9.6):

* Node -> v14.17.6
* npm -> 7.21.1

Como hacer una nueva release de la app:

* Hacer un sync del fork con el repo oficial
* Borrar ./plugins/ y contenidos de ./www
* Hacer los cambios necesarios en ```resources``` | ```moodle.config.json``` | ```config.xml```
* En el caso de perderlos obtener de nuevo ```google-services.json``` & ```GoogleService-Info.plist```
* ```ionic cordova platform remove ios``` & ```ionic cordova platform remove android```
* ```ionic cordova platform add ios``` & ```ionic cordova platform add android```
* ```NODE_ENV=production ionic cordova run ios --prod``` & ```NODE_ENV=production ionic cordova run android --prod```
* Deploy a app stores mediante Xcode y Android Studio
