# SEO Topics to Cover

1. Item Name vs Display Name
2. Link Manager
3. Meta Tags
4. Canonical + Duplicate Content
5. Bundling + Minification of Resources
6. Image Optimizations
7. Adaptive vs Responsive
8. 301 Strategy
9. General SEO

## Item Name vs Display Name

You don't want the items you create to have spaces in them, this will cause issues when linking to items and it will create consistency.  Typically we make a change to the item:save and item:rename events in Sitecore to take anything that the content manager has typed in and make it SEO Friendly for the Item Name, and then leave what they entered for the Display Name.

    namespace Site.Infrastructure.Events
    {
        public class ItemHandler
        {
            protected void OnItemAdded(object sender, EventArgs args)  
            {
                Item item = (Item)Event.ExtractParameter(args, 0);

                Set FriendlyItemName(item);
            }

            protected void OnItemRenamed(object sender, EventArgs args) 
            {
                Item item = (Item)Event.ExtractParameter(args, 0);

                SetFriendlyItemName(item);
            }
        }
    }
Patch Configuration Changes needed:

    <?xml version="1.0"?>
    <configuration xmlns:patch="http://www.sitecore.net/xmlconfig/">
      <sitecore>
        <events timingLevel="custom">
          <event name="item:added">
            <handler type="" method="" />
          </event>
        </events>
      </sitecore>
    </configuration>

If you don't do this, you will need to make sure the item name follows the following rules:

## Link Manager

    <?xml version="1.0"?>
    <configuration xmlns:patch="http://www.sitecore.net/xmlconfig/">
      <sitecore>
        <linkManager>
          <patch:attribute name="defaultProvider">custom</patch:attribute>
          <providers>
            <clear />
            <add name="custom"
                 type="site.Infrastructure.Managers.LinkManager, Site.Infrastructure"
                 addAspxExtension="false"
                 alwaysIncludeServerUrl="false"
                 encodeNames="true"
                 languageEmbedding="never"
                 languageLocaton="filePath"
                 shortenUrls="true"
                 useDisplayName="false"
                 lowercaseUrls="true" />
          </providers>
        </linkManager>
      </sitecore>
    </configuration>
    
It's important to have the link manager defined, so that the links on your site follow a consistent naming convention.  Without the use of the Link manager, you might end up links on some parts of your site that link to /en/home and others that just link to the / for the homepage.

## Meta Tags

- Meta Title (Single-Line Text)
- Meta Description (Multi-Line Text)
- Meta Keywords (Multi-Line Text)

Should create a base or interface template that can be inherited by any page type templates.

Show an Example in Example Project

## Canonical + Duplicate Content

By Default Sitecore creates dozens of urls for the same page.  With the use of canonical Url tag in the browser, you can instruct to Google, which is the original page.

Example Urls:

- http://www.somesite.com/home
- http://www.somesite.com/home.aspx
- http://www.somesite.com/en
- http://www.somesite.com/en/home
- http://www.somesite.com/en/home.aspx
- http://www.somesite.com/?sc_lang=en
- http://www.somesite.com/sitecore/content/home
- http://www.somesite.com/sitecore/content/home.aspx
- http://www.somesite.com/en/sitecore/content/home
- http://www.somesite.com/en/sitecore/content/home.aspx

## Bundling + Minification of Resources

With the Use of .Net, bundling and minification of resources are made very easy.  To get started you need to define scripts that will go into the bundle.  You will need to define a bundle configuration.

## Image Optimizations

## Adaptive vs Responsive

## 301 Strategy

At some point you will want to 301 content for pages that you are removing from Sitecore, or just renaming.  You could do these changes in the IISRewrite Tool, but you may want to consider building or reusing a Sitecore Marketplace Package that allows the content manager to create 301's themselves.  (I will demonstrate an approach to doing this in another video session)

## General SEO

- Alt Tags for Images
- Using the Correct Header Tags and having cleaner code