# Angular 4 cheatsheet.
This is a repository for various feature implementation and brief angular 4 feature documentation.

# Getting started.
 - Install `node.js and npm`
 - Install Angular CLI `npm install -g @angular/cli`
Optional
 - Install pug cli `npm install -g pug-cli`
 
# create new project
 - `cd path/to/your/dev/dir`
 - and `ng new <meaningful-appname>` and wait for cli to install.
Optional
 - `cd <meaningful-appname>`
 - and `npm install --save @angular/material hammerjs @angular/cdk` for angular material.

# test server
 - `cd path/to/project/dir`
 - `ng serve`

# To learn
 - TypeScript
 - Pug

# create new component
`create new file '<your-component>.component.ts'
```
    import {Component} from '@angular/core';
    @Component({
        selector:'a-new-tagname',
        template:'<span> Hello world </span>'
    })
    export class MyComponent{
        constructor(){
            //I'm up.
        }
    }
```
`Including external template and styles`

 - Files
```
... \app.component.ts
    \app.component.html
    \app.component.css
```
 - Component
```
    ...
    @Component({
        selector:'a-new-tagname',
        templateUrl : './app.component.html'
        styleUrls:['./app.component.css' /*, 'morestyles.css'*/]
    })
    ...
```

# Injectable / Service 
`app.service.ts`
```
import {Injectable} from '@angular/core';

@Injectable()
export class MyService{
    constructor(){
        // do something
    }
}

```
# using http services with injectable

`app.module.ts`
```
import {HttpModule} from '@angular/http';
@NgModule({
  imports: [
    HttpModule
  ],
})
export class AppModule{}
```

`app.service.ts`
```
import {Injectable} from '@angular/core';
import {Http} from '@angular/http';

@Injectable()
export class MyService{
    constructor(private _http:Http){
        // do something
    }
}
```

# Injecting a service to a component

`app.module.ts`
```
import {HttpModule} from '@angular/http';
import {MyService} from './app.service';

@NgModule({
  providers: [
    MyService
  ],
})
export class AppModule{}
```
`app.component.ts`
```
import {Component} from '@angular/core';
import {MyService} from './app.service';

@Component({ ... })
export class MyComponent{
        constructor(){
            //do something
        }
}

```
