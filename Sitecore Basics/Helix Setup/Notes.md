# Helix Setup

Why use Helix?

It's considered best practice by Sitecore.  

What is it?

It's a framework or general rule of how 

What is it not?

It's not a technical requirement.  So if you want to use Glass, than you can use Glass, or Unicorn or anything else for that matter.

So what is Habitat?

It's just an example site to use as a reference.  It is not a starter kit that you should use for developing your first Helix implementation.  It is however a good reference to see how you should built a Helix implementation.  And there are things within Habitat that will make sense reusing in your own implementation

## What Am I Building:

Basic Helix Implementation from Scratch
It will use and I will demonstrate setting up Unicorn for Serialization, but you could definitely choose to use TDS.
Will not Use Gulp, and will demonstrate building from Scratch
It's a shell for future tutorials


## General Folder Structure

$/Helix-Example/
  - src
    - Foundation
      - Serialization
        - code
          - App_Config
          - Controllers
          - Repository
          - Models
          - Views
          - Web.config
          - serialization
          - tests
    - Feature
    - Project 

## General Solution Structure

- Solution
  - Configuration
  - Feature
  - Foundation
    - Serialization [Web Project]
  - Project
    - Helix [Web Project]

### Project
This layer is at the highest point and everything to do with the things you are building for a website should typically appear here.  Example, graphics, layouts and more that relate to a site you are building.

### Feature
This layer is probably one of the easiest to understand, since if you are building a Navigation module, that is a feature for your project and typically would appear in this layer.  

### Foundation
The lowest of the layers, and as the name suggests, it forms the foundation for your implementation.  You should think of it as a layer that should very seldom change, since it's used as a foundation for the other layers.  Example other tools such as Bootstrap, the Sitecore platform, jquery etc would be considered foundational elements.

In this tutorial we will setup the basis for serialization in our implementation for use with future projects.

## General Tips

zzz for app config naming convention so inheritance is correct.  One project vs multiple project setup.  Having a tests project and why that's separated.


## Discuss Multi-site and multi-tenant


