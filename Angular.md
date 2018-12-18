# Angular 
## What is Angular?
Angular is a javascript framework.

## Installing Angular
Go to nodejs.org and download the latest version - uninstall (all) installed versions on your machine first.
- https://nodejs.org

Depending on the CLI version you're using, you might also need to add the FormsModule  to the imports[]  array in your app.module.ts  file (add it if you don't see it there). 
If you don't have FormsModule  in imports[]  in AppModule , please do add it and also add an import at the top of that file: import { FormsModule } from '@angular/forms'; 

## Create project/component
ng new Project-Name
ng generate component ng g c

#### Updating npm:
Run [sudo] npm install -g npm  (sudo  is only required on Mac/ Linux)

#### Updating the CLI

[sudo] npm uninstall -g angular-cli @angular/cli 

npm cache clean 

[sudo] npm install -g @angular/cli 

### How to...
- How to add Bulma to Angular
* https://scotch.io/courses/build-your-first-angular-website/adding-bulma-css-to-an-angular-app
- How to add FontAwsome
* https://www.npmjs.com/package/angular-font-awesome
