# Demossr

 Demonstrate server side rendering process in angular 2+.
 [click here](http://angular-ssr.surge.sh/)

# Follow the following step:-

```sh
-> To integrate the ssr in angular.
        ng add @nguniversal/express-engine
-> To make the build.
        npm run build:ssr
-> To run the build.
        npm run serve:ssr
-> If show any error related to pwa then add pwa.
        ng add @angular/pwa --project *project-name*
```

```json
  "scripts": {
    "ng": "ng",
    "start": "ng serve",
    "build": "ng build",
    "test": "ng test",
    "lint": "ng lint",
    "e2e": "ng e2e",
    "dev:ssr": "ng run demossr:serve-ssr",
    "serve:ssr": "node dist/demossr/server/main.js",
    "build:ssr": "ng build --prod && ng run demossr:server:production",
    "prerender": "ng run demossr:prerender"
  }
```

# Some point to be noted:-
- Some time it also ask to enter the name of project in ssr ad the time of add command. See below:-
```shell
ng add @nguniversal/express-engine --clientProject myProjectName
```
- You can find the project name from angular.json file. See below:-
  ```json
{
  "$schema": "./node_modules/@angular/cli/lib/config/schema.json",
  "version": 1,
  "newProjectRoot": "projects",
  "projects": {
    "demossr": {   // This is your project name
      "projectType": "application",
      "schematics": {},
      "root": "",
      "sourceRoot": "src",
	  .
	  .
```
- It may happen that it will throw the error of *'**TypeError: Cannot read property 'ngOriginalError' of undefined'***
     - Basically this error is occur due to interceptor.
     - Go to the [link](https://www.w3resource.com/angular/server-side-rendering-an-intro-to-angular-universal.php) to see the correct steps to resolve the issue. 


# Screenshot

-> Right click on main content of website. 

-> Click on view page source.

-> Now you can see the content.


![](https://github.com/Rahul151995/ssr-angular/blob/master/pagesource.png)
