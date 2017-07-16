# MongoDB-Custom-Properties
Plugin to allow definition in Hackolade of custom properties for MongoDB target

<div class="main-content">

<span class="rvts6">For each object in Hackolade, we've defined a set of standard properties that appear in the properties pane.  But it is possible that your company wants to define and track additional properties for models, containers, entities, and attributes.  Hackolade let's you do just that, by leveraging our plugin architecture (used also to integrate our modeling engine with all kinds of NoSQL document databases.)</span>

<span class="rvts6">  
</span>

## <span class="rvts0"><span class="rvts16">1) Download and enable plugin</span></span>

<span class="rvts6">To enable the custom properties capability, you first need to download a plugin for each database target for which you wish to add properties.  To do so, go to Help > DB Target Plugin Manager</span>

![](lib/Plugin-managermenu.png)

<span class="rvts6">  
</span>

<span class="rvts6">You may choose which plugin to install on your computer.</span>

![](lib/Plugin-manageravailablecustomprops.png)

<span class="rvts6">  
</span>

<span class="rvts6">This will result in the plugin appearing in the Installed tab of the plugin manager.</span>

![](lib/Plugin-Managerinstalledcustomprops.png)

<span class="rvts6">  
</span>

## <span class="rvts0"><span class="rvts16">2) Access plugin configuration files</span></span>

<span class="rvts6">You are now ready to add custom properties via editing of configuration files.  The plugin configurations files can be found by going to Help > Show plugin directory:</span>

![](lib/Plugin-Showplugindirectory.png)

<span class="rvts6">  
</span>

<span class="rvts6">For each custom properties plugin, you will find the a directory structure similar to this one:</span>

![](lib/Plugin-CustomPropdirectorystructure.png")

<span class="rvts18">Notes:</span><span class="rvts6"></span>

<span class="rvts6">i) do NOT make any changes to the package.json file!  Only the <object>LevelConfig.json files should be edited according to the specifications below.</span>

<span class="rvts6">ii) It is advised to keep a backup of the files before making changes, so you can revert back in case of errors.</span>

<span class="rvts6">iii) it is always necessary to restart the application after having saved changes before you can see these changes relected in the properties pane.</span>

<span class="rvts6">iv) for field-level definitions, since field types have different property lists, it may be necessary to define custom properties for multiple field types.</span>

## <span class="rvts0"><span class="rvts16">3) Levels</span></span>

<span class="rvts6">As a reminder, terminology differs between NoSQL database:</span>

<span class="rvts6">- container means: dbs in MongoDB, region in DynamoDB, and bucket in Couchbase</span>

<span class="rvts6">- entity means: collection in MongoDB, table in DynamoDB, and document kind in Couchbase</span>

<span class="rvts6">- field means: field in MongoDB and Couchbase, and attribute in DynamoDB</span>

<span class="rvts6">  
</span>

<span class="rvts6">You need to edit the corresponding <object>LevelConfig.json file to add custom properties.</span>

<span class="rvts6">  
</span>

## <span class="rvts0"><span class="rvts16">4) Lower tabs</span></span>

<span class="rvts6">For each level, the Hackolade properties pane may have one or more lower tab:</span>

<span class="rvts6">- MongoDB model lower tab:</span>

![](lib/MongoDBmodellowertab.png)

<span class="rvts6">- MongoDB dbs lower tab:</span>

![](lib/MongoDBdbslowertab.png)

<span class="rvts6">- MongoDB collection lower tab:</span>

![](lib/MongoDBcollectionlowertab.png)

<span class="rvts6">- MongoDB field lower tab:</span>

![](lib/MongoDBfieldlowertab.png)

<span class="rvts6">  
</span>

<span class="rvts6">If the level allows multiple tabs, you need to choose to which lower tab you want to add properties.</span>

<span class="rvts6">  
</span>

## <span class="rvts0"><span class="rvts16">5) Property types</span></span>

<span class="rvts6">The following controls are possible for user-defined properties:</span>

![](lib/Plugin-possiblepropertytypes.png)

*   <span class="rvts6">simple text: one line of text</span>
*   <span class="rvts6">text area: popup for multi-line text entry</span>
*   <span class="rvts6">dropdown selection from a deined list of options</span>
*   <span class="rvts6">numeric-only field</span>
*   <span class="rvts6">checkbox: for true/false entry</span>  
    <span class="rvts6">  
    </span>

<span class="rvts6">  
</span>

## <span class="rvts0"><span class="rvts16">6) Property definition</span></span>

<span class="rvts6">Examples are provided in the comments section of each config file.  Here's an overview of the schema:</span>

![](lib/Plugin-propertyschema.png)

<span class="rvts6">Here's another view, consolidated:</span>

![](lib/Plugin-custompropsconsolidatedschema.png)

<span class="rvts6">- propertyName: mandatory, this is the property label that will appear in the Property Pane</span>

<span class="rvts6">- propertyKeyword: mandatory, this is the unique key for the property</span>

<span class="rvts6">- shouldValidate: optional, boolean true/false to define whether to validate the regular expression of the text input [default: false]</span>

<span class="rvts6">- propertyTooltip: optional, in the case of input types textarea and dropdown, it is possible to display a tooltip  defined here</span>

<span class="rvts6">- propertyType: mandatory, this is the control definition, with possible values: text, details, select, checkbox</span>

<span class="rvts6">- options: optional, this is the array of possible checkbox options</span>

<span class="rvts6">- template: optional, this is needed in the case of propertyType = details, to define a popup multi-line text.  Possible value: textarea</span>

<span class="rvts6">- valueType: optional, this is needed in to specify that a property is numberic only.  Possible values: numeric</span>

<span class="rvts6">  
</span>

</div>

</div>

</article>

</div>
