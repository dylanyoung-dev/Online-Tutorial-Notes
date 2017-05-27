# Yeoman Generator Notes

## Installation

Must have Node, NPM and Yeoman Installed on your machine

npm install "folder location of Yeoman Generator"

Create a Local Repository for the generator, and then use npm link when you are in the folder where the generators package.json file exists.

https://60devs.com/simple-way-to-manage-local-node-module-using-npm-link.html

Example.  In the C:\Git\Helix-Sitecore

I had the following package.json file:



## Common Functionality

generator.templatePath:

Will return .\templates by default, if you pass in a parameter it will append it.  Ex.

module.exports = class extends Generator{

    DoSomething() {
        this.templatePath('/Feature');

        // returns ./Templates/Feature
    }
}

generator.destinationPath:

Will return the destination where the templated code is going.  Again you can specify a parameter for this method which will append that to the path, ex.

this.destinationPath('/Feature/**')

Will return ".\project\Feature\**";

## Passing Options between Generator and Sub-Generator

ejs template syntax