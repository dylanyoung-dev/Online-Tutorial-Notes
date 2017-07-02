# Creating a Custom Save Action


1. Make sure WFFM is installed
2. Create a new class that inherits from Sitecore.Form.Submit.ISaveAction

3. Register that action for use with WFFM, by creating a new item at /sitecore/system/Modules/Web Forms for Marketers/Settings/Actions/Save Actions

The Template sits under /sitecore/templates/Web Forms for Marketers/Action/Submit Action

Assembly should match your project Assembly name
Class should match the class name + the namespace for that class

using System.Collections.Specialized
using Sitecore;
using Sitecore.Data;
using Sitecore.Data.Items;
using Sitecore.Form.Core.Client.Data.Submit;
using Sitecore.Form.Core.Controls.Data;
using Sitecore.Form.Submit;

public class PostToExternal(ID formId, AdaptedResultList fields, params object[] data) {

// fields.GetEntryByName("FirstName").Value

}