---
title: "Activity: Leaflet"
nav: Leaflet
topics: 
---
<svg xmlns="http://www.w3.org/2000/svg" width="220" height="220" fill="currentColor" viewBox="0 0 16 16" style="display:block;margin:1rem auto 1.5rem auto;">
  <path d="M8 0a8 8 0 1 0 0 16A8 8 0 0 0 8 0M3.668 2.501l-.288.646a.847.847 0 0 0 1.479.815l.245-.368a.81.81 0 0 1 1.034-.275.81.81 0 0 0 .724 0l.261-.13a1 1 0 0 1 .775-.05l.984.34q.118.04.243.054c.784.093.855.377.694.801-.155.41-.616.617-1.035.487l-.01-.003C8.274 4.663 7.748 4.5 6 4.5 4.8 4.5 3.5 5.62 3.5 7c0 1.96.826 2.166 1.696 2.382.46.115.935.233 1.304.618.449.467.393 1.181.339 1.877C6.755 12.96 6.674 14 8.5 14c1.75 0 3-3.5 3-4.5 0-.262.208-.468.444-.7.396-.392.87-.86.556-1.8-.097-.291-.396-.568-.641-.756-.174-.133-.207-.396-.052-.551a.33.33 0 0 1 .42-.042l1.085.724c.11.072.255.058.348-.035.15-.15.415-.083.489.117.16.43.445 1.05.849 1.357L15 8A7 7 0 1 1 3.668 2.501"/>
</svg>

## Introduction

In this activity, you will learn how to create an interactive map in Leaflet, using a template, and host that map on GitHub Pages. 

By the end, you will have learned how to:
- Create and edit a GitHub repository
- Use GitHub Pages to make a live website from a repository
- Use a GitHub Leaflet template, alongside a Google Sheets data file, to create a custom map
- Add and customize the points that appear on your
- Understand the principles behind adding data layers including lines and polygons to your map.

## Getting started

Before you begin, make sure you're logged into your GitHub and Google Drive accounts. 

This activity involves two main components: a **GitHub repository** containing code that is already set up to create a Leaflet map per your specifications, and a **Google Sheets document** in which you will specify the data you want specified on your map. 

To begin, you must first make your own personal copies of both of these. 

### Configuring your GitHub Repository

1. Open the [GitHub template](https://github.com/mrcummings/leaflet-maps-with-google-sheets){:target="_blank" rel="noopener"}. 
2. Near the top right of the page, click the green **Use this template** button then select **Create a new repository**. Give your repository a descriptive name -- this name will form part of the URL for your live website later. When you're done, click **Create repository**. 

    > Note: You may receive an email from GitHub about "exposed secrets" as soon as you create this repository. Just ignore it. In order to make this repository work alongside Google Sheets, I created a Google API key that is referenced in the code. GitHub is trying to warn you about a potential (very low) risk, but since it's my API key, it's my risk -- not yours.

    > This repository contains all the code you need to create a map and is set up to be able to display that map as a GitHub Pages website, but right now the website doesn't exist. 

3. To change that, go to **Settings** then find **Pages** in the menu bar along the left side of the page. 
4. Under **Build and deployment** change the **Branch** from **None** to **Main**. Hit **Save**. Wait 30 seconds or so, then reload the page. You should see a message at the top of the page starting with "Your site is live at..." followed by a URL. Open that URL in a new tab. 

    > You should see a map filled out with sample data. There are three kinds of data on the map: points, lines, and polygons. 

    > Now that your site is live, you have a little bit of housekeeping to do in your GitHub repository.

5. Copy the URL to your live site, then return to the GitHub repository. Click **Code** in the menu bar along the top.
6. Find **README.md** in your repository and click on it. 

    > The README is a document containing important information about what others can expect to find in your GitHub repository. One of the relevant pieces of information is the link to your live site. Take a look at the **Live links** section. Currently, the link is directing to my site. 

7. Find the **pencil** icon at the top of the document. This is how you edit files in GitHub. Click it. Under **## Live links (replace with your own)**, find the link next to **Leaflet Map** and follow these steps exactly: 
  - delete my GitHub URL 
  - paste in your own. 

    > Do not highlight my GitHub URL and paste without deleting. In most other applications this would replace what you've highlighted with what you're pasting, but that's not how it works in Markdown (.md) files. You will create a very confusing hyperlink where the text you've highlighted (the original URL) links out to your new URL.


8. Click the green **Commit changes...** button. A window will pop up prompting you to create a commit message and description. One of GitHub's biggest strengths is **version control:** every time a change is committed, or saved, that "commit" is documented so that you or your collaborators will be able to easily see what changes were made when. It's usually best to write a clear message explaining what you've changed, but for the sake of time it's fine to stick with the auto-generated commit message. Click **Commit changes**. 

### Configuring your Google Sheets document

1. Open the [Google Sheets template](https://docs.google.com/spreadsheets/d/1Dbh2YtVljfZihrq6V6NpULficKGZ0W12zKHSlaHnevU/edit?gid=0#gid=0){:target="_blank" rel="noopener"}. Click **File** then **Make a Copy**. 
2. Click the blue **Share** button, then change **General access** from **Restricted** to **Anyone with the link**. Click **Done**.
3. Go to **File**, then under **Share** select **Publish to web**. Click the blue **Publish** button. hit **Close** to close this window.

    > These changes allow your GitHub repository to successfully read the data contained in this sheet.

4. Copy the URL in your **Browser's URL bar**. It is very important that you copy this URL, and not the **Publish to the web** url or the **Copy link** URL under **Share**. The correct URL should end in `gid=0`.
5. Now, return to your GitHub repository. If you aren't on the repository homepage already, click **Code** to get there. 
6. Open the file named **google-doc-url.js**. Click the **pencil** icon to edit it. On the line starting with `var googleDocURL`, highlight and delete the existing URL and paste in your own. Be careful not to erase the apostrophes at either end of the URL. 
7. Click **Commit changes...** then click **Commit changes** on the next window. 

    > Now, your map is pulling data directly from your Google Sheet, not mine. However, currently both Sheets are identical, so you won't be able to tell the difference. We'll change that in the next step. 

---

## Editing your map

Return to your Google Sheet. You'll notice that this Sheet consists of six tabs: **Options**, **Points**, **Geocoding Details**, **Polylines**, **Polygons**, and **Notes**. You will be editing at least four of these tabs as you customize your map. For now, make sure you're on the **Options** tab. 

### Configuring the Options Tab

On this tab, you can edit basic info about the map and its settings. **Do not** delete or rename the cells in the first row and first column, as this will break your map. You will be making edits in the column labeled **Customize**. The column labeled **Setting** tells you what exactly you're editing.

The **Options tab** is divided into color-coded categories for diffent types of options. Make the following changes in the **Map Info** section:

1. Change the value of **Map Title** to whatever you'd like. 
2. Replace the **Map Subtitle** with your own, or delete it to leave it blank.
3. Change the position of your Map Title or turn it off completely in the **Display Title** field (valid entries are `topleft`, `topcenter`, and `off`).
3. Change the **Author name** to your own name
4. Optionally, add your email address or a personal website to **Author Email or Website**
5. Replace the link in **Author Code Repo** with the URL for your own GitHub repository

    > Now, return to your live site and refresh the page. You should be able to see the changes you've made. Most of these changes will appear either in the info at the top of the page, or the credits bar at the bottom. 

Now take a look at the other sections of the **Options** tab: **Map Controls**, **Point Map Controls**, **Table Controls**, and **Polyline Map Controls**. We will return to some of these later, but we don't have time to cover all of them. You can see descriptions of what each field changes in the **Hints** column, and you can return to explore these these settings later when you're working on your own. Note that many of these fields only accept certain inputs. You can click the **dropdown arrow** in a cell to see the full list of input values that field accepts.

### Adding points

Navigate to the **Points** tab in your Google Sheet. There are six records in this sheet, one for each of the six points currently displayed on the map. To replace this data with your own, you'll need to delete this data. 

To add your data, fill in the following information in each field:
1. **Group:** a category or label for a subset of your points. This will appear in your map's legend.
2. **Marker Icon:** By default, points are represented by teardrop-shaped markers on the map. This defines the icon that appears in that marker. You have three options:
    - Leave this field blank if you want no icon to appear inside the marker.
    - Choose an icon from [Font Awesome's Version 5 Free Icon Collection](https://fontawesome.com/v5/search?ic=free-collection){:target="_blank" rel="noopener"}. The value you enter into the field will be `fa-` followed by the name of the icon.
    - Use an image. This will entirely replace the marker. To do this, you must upload an image to the **media** folder in your GitHub repository. The value you enter into the field will be `media/image-name.png` where "image-name.png" is replaced with the actual name of your image. _For best results, use a square image of 64x64 pixels, saved as a PNG with an all-lowercase filename._
3. **Marker Color:** Choose from any of the colors listed on the [W3Schools Color Names page](https://www.w3schools.com/colors/colors_names.asp){:target="_blank" rel="noopener"}, or add your own color using a Hex code (e.g. `#C8102E`). Marker color will be black if you leave this field blank.
4. **Icon Color:** By default, this is black. Make sure the color you choose contrasts well with your Marker Color. White is often a good choice.
5. **Custom Size:** Leave blank unless you're using an image instead of a marker in the **Marker Icon** field. This field defines the dimensions of that image.
6. **Name:** The name of the place that can be found at this point.
7. **Image:** Optional. An image to go alongside the description in this point's pop-up. Images should either be hosted on an online image sharing service like Flickr, or be uploaded to the **media** folder of your GitHub repository. Leave this field blank if you don't wish to include an image.
    - For images hosted elsewhere online, simply paste the URL to that image in this field. 
    - For images in your **media** folder, use the format `media/image-name.png`, where "image-name.png" is replaced by the actual filename.
8. **Description:** Text that will appear in the pop-up. You can use HTML to enhance this text if you wish. Some examples of HTML tags you can add include: 
    - Line breaks: insert `<br>` anywhere you want two lines of text to be separated.
    - Hyperlinks: insert `<a href='https://digital.lib.iastate.edu/' target='_blank'>Digital Scholarship and Initiatives</a>` replacing the URL and link text with your own.
9. **Location:** This field isn't strictly necessary and isn't used anywhere in the map, but is a helpful reference for you. Use an address or a place name that describes exactly where this point is. 
10. **Latitude** and **Longitude:** These coordinates will tell Leaflet exactly where to place your map. You can find coordinates on [Google Maps](https://www.google.com/maps){:target="_blank" rel="noopener"} by searching for a location, then right-clicking its pin. You can also find coordinates by right-clicking anywhere on the map. Clicking on the coordinates that appear will copy them. Remember to separate the latitude (first) and longitude (second) in your data sheet.

Take a few minutes to some points to the map. If you can't think of any locations, or you don't want to hunt down coordinates right now, feel free to use the locations in the [Big 12 and 10 Institutions Sheet](https://docs.google.com/spreadsheets/d/1HO7PcBqLsqyDz2E329fpN65MbpiBELXncoE0p5wqU5I/edit?usp=sharing){:target="_blank" rel="noopener"} from our ArcGIS Online activity. 

When you're done, return to the **Options** tab. Under **Point Map Controls**, change the **Point Legend Title** to something fitting for the points you've added. 

Refresh your site to see the progress you've made. You may notice that the map _automatically updates_ its center point and zoom level so that all the points you've added are visible when the site loads.

### Lines and Polygons

This map doesn't just contain point data. There are also lines, representing trails and transit routes, and polygons, showing population density by county in East Coast states. 

Leaflet, and other open source mapping tools, use an open, semi-structured data format called **GeoJSON** to represent points and polygons. You can find GeoJSON files online, but they aren't always as easy to find as other geospatial data formats like shapefiles (.shp) and KML files. 

The sample data on this map includes three GeoJSON files for lines and one for polygons. You can access these in the **geodata** folder of your repository. 

In your Google Sheet, move to the **Polylines** tab. Here you can see how the line data is defined. 

Now, move to the **Polygons** tab. This tab is a bit more complex, with space to include information about how the data assigned to each polygon in your GeJSON files is represented on the map. 

If you don't wish to use any lines at all in your map, simply delete all everything _except row 1_ from the **Polylines** tab. 

If you don't wish to use any polygons in your map, delete everything in the **Customize** column of the **Polygons** tab _except the word "Customize" in row 1_.

If you do wish to use these types of data, you'll need to either create or find them. 

There are two web-based tools that can help you to do that: [Geojson.io](https://geojson.io/){:target="_blank" rel="noopener"} and [Mapshaper](https://mapshaper.org/){:target="_blank" rel="noopener"}. The greatest strength of Geojson.io is its ability to take lines and shapes you've drawn on a map yourself and convert them to a working GeoJSON file. Mapshaper allows you to import other geospatial data files and convert them to GeoJSON. 

If you're interested in learning more about either of these tools, check out the Hands-On Data Visualization tutorials on each below:

- [Draw and Edit with Geojson.io](https://handsondataviz.org/geojsonio.html){:target="_blank" rel="noopener"}
- [Edit and Join with Mapshaper](https://handsondataviz.org/mapshaper.html){:target="_blank" rel="noopener"}

---

## Future-proofing

Once you've created your map, there's one final step to ensure it will remain online and functional long-term. 

Earlier we discussed how the connection between Google Sheets and GitHub is made possible by my personal API key. I have no intentions of taking that key down now, but I can't guarantee it will remain active forever. Luckily, you have a way to remove the need for Google Sheets altogether. 

Only do this step when you're _absolutely certain_ that you no longer want to edit your data, unless you're willing to go through this step again each time you make edits. 

1. On your **Options** tab, click **File** then under **Download** select **Comma Separated Values (.csv)**. 
2. Find where your file downloaded and rename it exactly like this, including capitalization: `Options.csv`
3. If you used points, polylines, or polygons in your map, go to those tabs and download CSVs of each of them. Rename them exactly like this: `Points.csv`, `Polylines.csv`, `Polygons.csv`. 
4. In your GitHub repository, open the **csv** folder and upload each of your CSV files to it by clicking **Add file** then **Upload files**. 

    > Now your data is uploaded to your GitHub repository alongside your code, but the site doesn't know yet to pull data from the CSVs instead of the Google Sheet. 

5. Return to your repository homepage by clicking **Code**. Open the **google-doc-url.js** file. 
6. Click the **pencil** icon to edit the file. Replace the Google Sheets URL, including the surrounding apostrophes, with the word "null". The line should look like this:
    `var googleDocURL = null;`
7. (Optional) delete the line containing the Google API key. 
8. When you're finished, **commit changes**. Now, the map on your site should be pulling its data from the CSV files in your repository, not Google Sheets.

---

## Credits

This activity is heavily based on _Leaflet Maps with Google Sheets,_ part of Chapter 12 of Hands-On Data Visualization by Jack Dougherty & Ilya Ilyankou. 