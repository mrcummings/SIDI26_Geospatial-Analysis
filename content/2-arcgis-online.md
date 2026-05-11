---
title: "Activity: ArcGIS Online"
nav: ArcGIS
topics:
---
<svg xmlns="http://www.w3.org/2000/svg" width="220" height="220" fill="currentColor" viewBox="0 0 16 16" style="display:block;margin:1rem auto 1.5rem auto;">
  <path d="M8 0a8 8 0 1 0 0 16A8 8 0 0 0 8 0M4.882 1.731a.48.48 0 0 0 .14.291.487.487 0 0 1-.126.78l-.291.146a.7.7 0 0 0-.188.135l-.48.48a1 1 0 0 1-1.023.242l-.02-.007a1 1 0 0 0-.462-.04 7 7 0 0 1 2.45-2.027m-3 9.674.86-.216a1 1 0 0 0 .758-.97v-.184a1 1 0 0 1 .445-.832l.04-.026a1 1 0 0 0 .152-1.54L3.121 6.621a.414.414 0 0 1 .542-.624l1.09.818a.5.5 0 0 0 .523.047.5.5 0 0 1 .724.447v.455a.8.8 0 0 0 .131.433l.795 1.192a1 1 0 0 1 .116.238l.73 2.19a1 1 0 0 0 .949.683h.058a1 1 0 0 0 .949-.684l.73-2.189a1 1 0 0 1 .116-.238l.791-1.187A.45.45 0 0 1 11.743 8c.16 0 .306.084.392.218.557.875 1.63 2.282 2.365 2.282l.04-.001a7.003 7.003 0 0 1-12.658.905Z"/>
</svg>

## Introduction

In this activity, you will learn the basics of how to create a map using ArcGIS Online. By the end, you'll know how to:
- Navigate to the ISU ArcGIS Online homepage and log in
- Find pre-existing data and add your own data
- Change how the data on your map is visualized
- Save and share your map
- Generate HTML embed code and export static images to use your map outside of ArcGIS Online

---

## Getting Started

As an Iowa State University student, you have free access to ArcGIS Online through the [ISU GIS Facility](https://www.gis.iastate.edu/){:target="_blank" rel="noopener"}. In order to access your free account, navigate to the [ISU ArcGIS Online Homepage](https://isugisf.maps.arcgis.com/){:target="_blank" rel="noopener"}.

If you aren't already logged in, you'll be prompted to log in using your ISU netID and password. 

Once logged in, click **Map** in the nav bar at the top of the page.

---

## Navigating the Map Viewer interface

You'll find yourself on a screen with a blank map of the world in the center, and two menu bars along the left and right sides. The central area is where you'll create your map. The map that's currently displaying is the basemap. 

The menu bar on the left side is called the **Contents toolbar**. Its options are mostly organizational. Here you can find and add layers of data to your map, change the basemap, configure your legend, save your map, create embed codes and static images, and more. Clicking on most of these options will open a pane immediately to the right of this toolbar. 

The menu bar on the right side is called the **Settings toolbar**. Here you will primarily work with specific data layers, altering what variables are displayed and how they are visualized, configuring pop-ups, and doing light analysis. You can't click on any of these yet because we haven't added any data, but once we've added a layer, clicking on each of these will open a pane immediately to the left of the toolbar.

---

## Finding data

ArcGIS Online contains a vast amount of geospatial data built in and free for you to use. To find data that already exists in that platform, open the Layers pane and click **Add**. 

There are a number of containers in which you can search for data on this platform. By default, you're searching **My content** -- which is where any content you've created lives. If this is your first time using ArcGIS Online, the pane will be empty. 

Clicking on **My content** will open a dropdown with other locations to search. **My favorites** shows you any layers you've bookmarked. **My groups** shows content created as part of group projects. **My organization** searches any content created and made available by anyone at ISU. These are all useful in certain contexts, but they won't be your go-to sources for data most of the time. 

The options you'll use most frequently are **ArcGIS Online** and **Living Atlas**. Click on **ArcGIS Online**.

Here, you're searching any content created and made publicly available by anybody in the world with an ArcGIS Online account. There is an enormous amount of content here, making it a valuable resource, but because anyone can contribute to it, it's important to use caution when choosing layers to use. 

There are four things to look for when evaluating a layer in ArcGIS Online. 
1. Who published this layer? 
  - The **publishing account** is listed at the bottom of the layer's info card. Data published by Esri, by national, state, or local governments, or by trusted non-profit groups, is often high quality. If you don't recognize the name of the publishing account, it's worth searching for information about them independently. 
2. Is the data "Authoritative?"
  - A **green checkmark badge** on a layer means that the publishing organization has rated the data as "Authoritative," usually meaning it represents their newest, best, and/or most high quality data available. This badge on a layer published by a trustworthy organization is a good sign.
3. Is it a part of Living Atlas?
  - Some layers are marked with a **blue globe badge**. These have been included in Esri's ArcGIS Living Atlas of the World, a highly curated collection of data layers. To pass review, these layers must meet high standards for quality of data and documentation. This is one of the most reliable signs that you've found good data.
4. What details are given about this layer?
  - Clicking the title of a layer will open a new pane with information about that layer. A good layer will have a detailed summary and description of exactly what kind of data you'll find in the layer.

 At the top of the **Add layer** pane, click on **ArcGIS Online**. If you select the **Living Atlas** option, you can search for only data that has been included in this collection. This is a great place to start searching for any data. 

 In the search bar, type in **ACS population**. Find the layer titled **ACS Population (Latest). 
 
 _Question:_ Examine the information you can see about this layer. Can you trust this dataset? Why or why not?

 Click the **add** button for this layer. Two things will happen. First, the data will automatically display on the map. Second, the **Properties** pane will open on the right side of your screen. click the **back arrow** net to **Add layer** in the pane on the left side. In the **Layers** pane, you can see that a layer called **ACS Population (Latest) has been added to your map. Click the arrow next to the layer title to see that there's actually three sub-layers in this dataset representing data at the state, county, and census tract levels. Zoom in on the map to see data displayed at each level.

 In the **Layers pane**, click on the three dots next to the State layer. Select **Show table**. This is the actual structured dataset that the data on the map is based on. Scroll through the data to see what variables are included. Close the table by clicking the X at the top right of the **Table pane** when you're done. 

 _Question:_ What variable is currently being displayed on this map?

_Question:_ take a look at the county-level map. What outliers do you see in the data?

---

## Adding your own data to the map

You can easily create data for point-based layers yourself. 

Open this [data spreadsheet](https://docs.google.com/spreadsheets/d/1HO7PcBqLsqyDz2E329fpN65MbpiBELXncoE0p5wqU5I/edit?usp=sharing){:target="_blank" rel="noopener"}.

This dataset contains information about universities that are members of the Big 12 and Big 10 conferences. Crucially, exact locations of each university are represented in the dataset by _latitude_ and _longitude_ variables. 

When you're creating your own dataset, you can easily find coordinates using [Google Maps](https://maps.google.com/){:target="_blank" rel="noopener"}. Search for a location you're interested in, right-click the pin, and click on the coordinates that pop up to copy them to your clipboard. Remember: this will copy both the latitude and longitude. When you paste this data into your spreadsheet, you'll need to separate the two values. 

When you have a complete dataset that you're ready to use, you'll need to export it as a CSV. In Google Sheets, click **File** then under **Download** select **Comma Separated Values (.csv)**. Locate the file where it was saved on your computer.

Now, return to Map Viewer. Click on **Add** at the top of the **Contents toolbar**. Select **Add layer from file**. Choose **Your device** and find the CSV wherever you saved it. 

On the next screen, choose **Create a hosted feature layer and add it to the map** and click **Next**. 

On this screen, you can assign data types for each of your variables. ArcGIS Online will try to automatically choose the best data types. For the most part, it's usually accurate but there's one change we should make: in the data type dropdown next to **year_founded**, select **String**. 

_Question:_ Why do we want to do this?

Click **Next**. On this screen, you'll specify where Map Viewer gets its location information. It should automatically identify your latitude and longitude fields. Click **Next**.

You can change the layer's title and add categories, tags, and a summary if you wish. If you think that others will want to use this data, it's a very good idea to be as descriptive as you can here. For now, we'll just click **Create and add to map**. 

You should now see a point-based layer with the locations of each university included in the dataset on your map. 

_Question:_ Does this data enhance your understanding of the outliers we identified previously?

---

## Changing variables and visualizations

In the **Layers pane** click on **County**. The **Properties pane** on the right should automatically update to display information about that data layer. 

Click on **Styles** in the **Settings toolbar**. Under **Choose attributes**, you can change which variable is being displayed on the map. Click the **X** next to the variable name. Once the map resets, you can click **+ Field** to choose a new variable. Let's choose **Total Population**. 

Now, instead of displaying data about the percent of the population in dependent age groups, instead we're looking at data about the total population of each county. Map Viewer provides many different visualization styles for your data: Counts and Amounts (color), Counts and Amounts (size), Dot Density, etc.

_On your own:_ Try two or three different styles. Be prepared to answer these questions: 
- Do you think any of these represents your data better or worse? 
- Do some work better visually with the other data layer on the map than others?

Once you've selected a style, you can click on **Style options** to customize the look of your map further. Your **Theme** will determine how colors are applied to the data. **Symbol style** allows you to choose a color pallette. **Data range** lets you adjust the values assigned to each color in your gradient. **Use caution when adjusting this range!** It's very easy to create a misleading map by moving these sliders too far in one direction or another.

When you're happy with how this layer looks, hit **Done**.

---

## Creating informational pop-ups

You may have noticed by now that if you click on a county on this map, a pop-up with some information about the county appears. In layers you find in ArcGIS Online, especially ones from Living Atlas, these pop-ups are likely to already be highly detailed -- but for data you add yourself, the pop-up will simply consist of a basic data table. 

These pop-ups are highly customizable. To edit the pop-ups for our universities layer, click on that layer in the **Layers pane** and then select **Pop-ups** in the **Settings toolbar**. 

In the **Pop-ups pane** that opens on the right, click on **Title**. The title consists of two parts: the name of the layer with a colon, and the word "name" in curly brackets. These curly brackets allow you to call the variables of specific variables from your data tables. Take a look at the title of one of your pop-ups: you can see that it's pulling in the name of that specific university in the title field. 

We can use this curly bracket syntax to our advantage to create our own custom pop-ups. Find **Fields list**, click the three dots, and select **delete**. This was the field that defined the data table in our pop-up. Let's replace it by clicking **+ Add content** and choosing **Text**. 

In the text box that opens up, you can write a descriptive sentence using variable names. Try pasting in this text:

>{name} is a {type} university located in {city}, {state}. It was founded in {year_founded} and has a student population of {student_pop_f23}. It's a member of the {conference} Conference. 

Now, the pop-up includes your custom text, with appropriate values replacing the variable names you input. 

You can do a lot more with pop-ups, including adding images, charts, and more. A good way to learn is to examine how pop-ups from layers found in Living Atlas are constructed, and try to recreate these on your own. 

---

## Saving and sharing your map

Unlike many other web-based tools, Map Viewer doesn't save your work automatically. Without saving, you're at risk of losing all your progress.

In the **Contents toolbar**, click **Save and open**. Choose **Save as**, and give your map a title. Once again, for a map you'd like other people to use, it's important to put descriptive information in the Categories, Tags, and Summary fields. When you're done, hit **Save**.

Once the map has been saved, in the future you can save it again by navigating to **Save and open** once more, but this time selecting **Save**, instead of **Save as**. 

Once your map has been saved, you can always return to it by navigating to the [ISU ArcGIS Online Homepage](https://isugisf.maps.arcgis.com/){:target="_blank" rel="noopener"} and selecting **Content** from the nav bar. 

Now your map is saved, but you are still the only person who can see it. If you want the map to be visible to others, you must adjust your Sharing Settings. 

In the **Contents toolbar**, select **Share map**, then **Manage sharing**. You'll see three sharing levels: **Owner**, **Organization**, and **Everyone (public)**. Currently, your map is set to **Owner**, meaning that only you, the creator and owner of the map can view it. 

If you set the map to **Organization**, anyone with an ISU ArcGIS Online account can view it. 

If you set the map to **Everyone (public)**, anyone on the internet can view it. 

You can change sharing settings at any time. Right now, let's make our maps available to Everyone and hit **Save**. 

You should see a pop-up warning you that not every layer is visible on your public map. This is an important distinction to keep in mind. The data layer we created and added to our maps has its own, separate, sharing settings than the map itself and was not updated automatically. To update it, click **Review sharing** then **Update sharing**. This will bring that layer's sharing settings in line with the map's. 

Finally, you have three ways to actually use this map. 

- First: The simplest way to use your map is to share a link to the map with others. You can get a shareable link by clicking **Share map** and selecting **Copy link to map**. You should check this link in a private browser window to see how it will look to someone not logged into your account. 

- Second: If you wish to include your map in a published paper, slideshow presentation, or poster, you'll want to create a static image of a portion of the map. In the **Contents toolbar**, select **Print**. This will open a **Print pane** where you can choose the size of the final image, the file format, and what else is included (legend, scale bar, author name, and more). You can create as many of these as you want, showing different aspects of the map.

- Third: If you want your audience to be able to utilize the interactive features of your map, but you'd rather display the map on your personal site, a course site, or any other website, you can create embed code. In the **Contents toolbar**, click **Embed map**. Choose your preferences from the available options, and when you're done click **Copy HTML**. Simply paste this into the HTML file for your site, or the appropriate location on your website editor of choice.

---

## On your own

Create a new map by selecting **Save and open** and clicking **New map**. Using the skills you've just learned, do the following:
- Find a high-quality dataset and add it to your map
- Choose a variable other than the default to display on the map
- Choose a visualization that you think works best for that variable
- Save the map

Be prepared to answer the following questions:
- What dataset did you choose and why? 
- What variable did you choose to display?
- What choices did you make about how to display that variable, and why?