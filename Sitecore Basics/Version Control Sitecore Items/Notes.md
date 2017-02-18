# Sitecore Basics : Version Control Sitecore Items

The purpose of this tutorial will be to describe the different version control options a developer has when they want to provide source control on the items they are creating within the Sitecore CMS.

## Slide Deck Notes

1. Title
2. Introduction - Who Am I?
3. Options
    * Unicorn
    * TDS Class (by HedgeHog)
    * Serializing + Deserializing Items
    * Item Packages
4. Unicorn
	* Benefits
		* Open Source Support
		* Large Community Support
		* New Features
	* Negatives
5. TDS Classic
	* Benefits
		* Wide Acceptance
		* Good Support
	* Negatives
		* Requires all developers to have a License
		* 
6. Serializing + Deserializing Items
	* Benefits
		* Very easy to perform, and great in one off situations
	* Negatives
		* Will lead to lost changes

	This approach is not ideal, unless you need to pull items from an external system once in awhile.  As a long term strategy, this will lead to confusion and headaches.

7. Item Packages
	* Benefits
		* Can be an ideal option for one off deployments of new features.
	* Negatives

	This approach isn't ideal either, because it will lead to synchronization issues with merging items.  If user A works on the Home item, and user A packages the change, and then user B does the same, there would no doubtably be conflict issues when the developers try to merge the changes.

## Demo Notes

Will Demo configuration of a basic setup using Unicorn, since it's the best option and because it's free to use.

We will use the Example Site project to demo how to configure Unicorn to track our items from the database to Source Control (Git).