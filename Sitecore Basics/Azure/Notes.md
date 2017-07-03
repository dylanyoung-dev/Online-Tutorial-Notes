# Azure with Sitecore

Get Prebuilt Arm Templates here: https://github.com/Sitecore/Sitecore-Azure-Quickstart-Templates

Also a great Arm Visualizer is http://armviz.io/



## ARM Template Types

### XPO

The Sitecore Experience Platform, running as a single WebApp instance.  Use this configuration for development and testing.  For security and scalability reasons, it is best practice to use the XM1 or XP1 configuration in production environments.

### XM

The Sitecore Experience Management configuration running both the CD and CM roles. Use this environment when you are not planning to use the Analytics and Marketing features of the Sitecore Experience Platform (also known as CMS-only mode).

### XP

The Sitecore Experience Platform configuration running four roles: CD, CM, Processing and Reporting.  Use this environment when you are planning a fully feature Sitecore Experience Platform installation.

### XDB

This Sitecore Experience Database configuration running both the Processing and Reporting roles.  Use this environment in combination with ann on-premise Sitecore XM installation to provide the Experience Database feature.