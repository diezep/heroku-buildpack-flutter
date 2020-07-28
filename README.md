# Heroku buildpack for Flutter
This buildpack for Flutter developers. Deploy your Flutter Web projects on Heroku easily.

## 🔨 Setup
#### 1. Add this buildpack in your Heroku app.
   You can copy the [link](https://github.com/diezep/heroku-buildpack-flutter) of this repository and paste it in buildpacks or write **diezep/flutter** and will be added automatically.
#### 2. Add PHP buildpack in your Heroku app.
   Is necessary add PHP buildpack **after** this buildpack. 
   
   PHP Buildpack is needed to run the static files in a web service that can be opened in browsers.
   *You can skip this step if you have another way to deploy statics files, like NodeJS, Flask..*

#### **IMPORTANT:** 
  By default, this buildpack get the **last version** of Flutter automatically, sometimes because is on beta channel, that version may have problems to compile a project with web support. 
  
  If this is your case, you can try downgrade the Flutter version manually, add FLUTTER_VERSION variable in your Heroku environment with the number of the most recent version that are currently working correctly.
  
** [UPDATED] Last working version: ** 1.19.0-4.3.pre

And that's it, your web page will be ready in a few minutes.
