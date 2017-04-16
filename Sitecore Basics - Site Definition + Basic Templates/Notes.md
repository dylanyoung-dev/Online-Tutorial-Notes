# Site Definition File

```xml
<configuration xmlns:patch="http://www.sitecore.net/xmlconfig/">
  <sitecore>
    <sites>
      <site name="ExampleSite"
            patch:after="site[@name='modules_website']"
            targetHostName="example-82"
            database="web"
            virtualFolder="/"
            physicalFolder="/"
            rootPath="/sitecore/content/example-site"
            startItem="/home"
            domain="extranet"
            allowDebug="true"
            cacheHtml="true"
            htmlCacheSize="50MB"
            registryCacheSize="0"
            viewStateCacheSize="0"
            xslCacheSize="25MB"
            filteredItemsCacheSize="10MB"
            enablePreview="true"
            enableWebEdit="true"
            enableDebugger="true"
            disableClientData="false"
            cacheRenderingParameters="true"
            renderingParametersCacheSize="10MB" />
    </sites>
  </sitecore>
</configuration>
```

Should mention going to site.com/sitecore/admin/showconfig.aspx to see the output of patch configs to the main web.config

Not a Helix Approach

## Attributes I'm Leaving out till future videos

1. dictionaryPath = "/sitecore/content/habitat/global/dictionaryPath
2. dictionaryAutoCreate = "false"
3. enableItemLanguageFallback = "true"
4. formsRoot = "{Guid}"

## Types of Items + Templates to Create

1. Site Folder Template / Item (sitecore/content/example-site)
2. Home Template / Item (sitecore/content/example-site/home)
3. Global Template / Item (sitecore/content/global)