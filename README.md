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

# To learn
 - TypeScript
 - Pug

# create new component
`create new file '<your-component>.component.ts'
```
    import {Component} from '@angular/core';
    @Component({
        selector:'a-new-tagname'
    })
    export class MyComponent{
        constructor(){
            //I'm up.
        }
    }
```


