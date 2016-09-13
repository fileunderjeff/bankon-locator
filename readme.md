This is a bank locator for Bank on Houston and Bank on Montgomery County. The "Bank Ons" provide a network of financial services for at-risk populations.

This is based on http://www.bjornblog.com/web/jquery-store-locator-plugin

There are three things you need to do to get this up and running:

# Google Maps API Key

Drop it in the URL of line 61 of index.html.

# Get your data together

Get your bank info into a CSV file. Convert it to XML using http://www.convertcsv.com/csv-to-xml.htm

In order to create a properly formatted XML file for this locator, use the following format in Step 4 of that site:

Top:
<root>

Repeating section:
<marker {h1}="{f1}" {h2}="{f2}" {h3}="{f3}" {h4}="{f4}" {h5}="{f5}" ... />

Bottom:
</root>

Make sure that the repeating section has the same number of fields as your CSV file. 

Use this output as data/locations.xml.

# Update the info windows

/assets/js/plugins/storelocator/templates
location-list-description.html is what appears in the sidebar
infowindow-description.html is what appears in the pop up window

Swap out variables with the names of your rows.