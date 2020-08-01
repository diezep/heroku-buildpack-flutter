# Heroku Buildpack for Flutter
![header](https://user-images.githubusercontent.com/38699812/89092029-fb5b8400-d373-11ea-8ac0-6a46c817ae3b.png)
Automate your deployments on Heroku easily.

## 🔨 Setup

#### Add this Buildpack in your Heroku app 

   You can copy the [link](https://github.com/diezep/heroku-buildpack-flutter) of this repository and paste it in buildpacks or write **diezep/flutter** and will be added automatically.

#### Optional

   You can add optional [environment variables](#--environment-variables) to customize the deployment of your project but nothing is required, all are optional.
   
#### Problems to compile
  By default, this buildpack get the **last version** of Flutter automatically, sometimes because is on beta channel, that version may have problems to compile a project with web support. 
  
  If this is your case, you can try downgrade the Flutter version manually, add FLUTTER_VERSION variable in your Heroku environment with the number of the most recent version that are currently working correctly.
  
**Last working version :** 1.19.0-4.3.pre
   
## 🚩 TODO :

### Environment variables :

* [x] VERSION to set the name of custom version of Flutter.
* [x] CLEANUP to remove uneccessary files after the build.
* [ ] CACHE to remove and download every file its need to compile the project in every deploy.
* [ ] SUBDIR to ubicate the project if it isn't in a root directory.

### Features :

* [x] No more PHP Buildpack needed.
* [x] Save and restore Flutter and Dart SDK in cache.
* [x] Save and restore [dhttpd](https://github.com/diezep/dhttpd) in cache.
* [ ] Save and restore project dependencies needed in cache.

## 🚧 Environment variables:

All variables were built following the structure **FLUTTER_VARNAME** to identified easily in Heroku configurations. If you want to use some variable, remember **use the structure** following to the variable.

| Variable |   Type  |   Default        |  Description
|----------|---------|------------------| -------------------|
| CLEANUP  | *boolean* |  <center>true</center> |Remove **uneccessary files** of your project after the compile. |
|  VERSION | <center>*string*</center> | *Last version in [beta channel](https://flutter.dev/docs/development/tools/sdk/releases?tab=linux).* | The **name of the version** you want to use to compile the project.| 

### Set variable
   Example of setting CLEANUP var in Heroku CLI:
   ```shellscript
   $ heroku config:set FLUTTER_CLEANUP=true -a project-name
   ```
### Example

The next image is an example of setting environment variables following the structure mentioned above :

![example_use_in_variables](https://user-images.githubusercontent.com/38699812/89090700-42447c00-d36a-11ea-8148-84af7cddfa21.PNG)

<!-- TODO: ## 📌 LICENCE -->
<!-- TODO: ## 📌 CONTRIBUTE -->

## 📝 Final note
   This buildpack is unofficial that means i don't have any conection with Heroku or Google from Flutter developer team <!--Although I would like belonging to any of the two :D -->. This repository was made as a hobby, i'm always interested in learn new things, this is one demostration of that :)