---
title: What is Geospatial Analysis?
nav: Lesson
topics: GIS concepts; Spatial data; Maps
---
<svg xmlns="http://www.w3.org/2000/svg" width="220" height="220" fill="currentColor" viewBox="0 0 16 16" style="display:block;margin:1rem auto 1.5rem auto;">
  <path d="m10.495 6.92 1.278-.619a.483.483 0 0 0 .126-.782c-.252-.244-.682-.139-.932.107-.23.226-.513.373-.816.53l-.102.054c-.338.178-.264.626.1.736a.48.48 0 0 0 .346-.027ZM7.741 9.808V9.78a.413.413 0 1 1 .783.183l-.22.443a.6.6 0 0 1-.12.167l-.193.185a.36.36 0 1 1-.5-.516l.112-.108a.45.45 0 0 0 .138-.326M5.672 12.5l.482.233A.386.386 0 1 0 6.32 12h-.416a.7.7 0 0 1-.419-.139l-.277-.206a.302.302 0 1 0-.298.52z"/>
  <path d="M8 0a8 8 0 1 0 0 16A8 8 0 0 0 8 0M1.612 10.867l.756-1.288a1 1 0 0 1 1.545-.225l1.074 1.005a.986.986 0 0 0 1.36-.011l.038-.037a.88.88 0 0 0 .26-.755c-.075-.548.37-1.033.92-1.099.728-.086 1.587-.324 1.728-.957.086-.386-.114-.83-.361-1.2-.207-.312 0-.8.374-.8.123 0 .24-.055.318-.15l.393-.474c.196-.237.491-.368.797-.403.554-.064 1.407-.277 1.583-.973.098-.391-.192-.634-.484-.88-.254-.212-.51-.426-.515-.741a7 7 0 0 1 3.425 7.692 1 1 0 0 0-.087-.063l-.316-.204a1 1 0 0 0-.977-.06l-.169.082a1 1 0 0 1-.741.051l-1.021-.329A1 1 0 0 0 11.205 9h-.165a1 1 0 0 0-.945.674l-.172.499a1 1 0 0 1-.404.514l-.802.518a1 1 0 0 0-.458.84v.455a1 1 0 0 0 1 1h.257a1 1 0 0 1 .542.16l.762.49a1 1 0 0 0 .283.126 7 7 0 0 1-9.49-3.409Z"/>
</svg>

---

## Why maps?

Maps are a rare type of data visualization. An effective map allows you to connect your data to place: not just "something has happened," but "something has happened here, not there." This allows you look for answers and make arguments about _how_ places and your data are connected.

{% include figure.html img="snow-map.jpg" alt="John Snow's 1854 map of cholera deaths in a neighborhood in London" caption="John Snow's 1854 cholera map. Right-click to open a larger image in a new tab. <br>Source: Wikimedia Commons" width="75%" %}

In 1854, Dr. John Snow mapped cholera deaths in London by location. This revealed deaths clustered around a single water pump, indicating that contaminated water was the source of the outbreak. The data, plus the map, plus the argument fundamentally changed how the spread of disease is understood.

Spatial questions are relevant to every discipline:
- Where do things happen, and where don't they?
- How does proximity affect data patterns?
- How do patterns change from place to place, or over time?

---

## What makes data geospatial?

Not all data is spatial, but almost any data can be if location is relevant.

| Data type | What it describes | Examples|
|---|---|---|
|**Spatial data** | _where_ a feature is located | coordinates, addresses, place names |
|**Attribute data** | _what_ a feature is like | population, land use, temperature |

<br>
Geospatial data combines both a location (spatial data) and something meaningful about that location (attribute data).

**Question:** What data from your own research or classwork might have a spatial dimension that you haven't explored yet?

---

## Vectors, Rasters, Basemaps

Spatial data comes in two formats. Many maps use both.

**Vector data** represents distinct features using geometry
- **Points:** addresses or exact geographic coordinates where something exists or has happened
- **Lines:** connections between points that represent linear features like roads or rivers
- **Polygons:** enclosed shapes that represent the boundaries of areas like states, counties, or land parcels

In vector data, attributes are often represented by changing the colors or sizes of the points, lines and polygons. Two lines of different thicknesses could represent rivers of more or less volume. Two polygons colored red and blue could indicate winners of an election.

**Raster data** represents phenomena as a grid of pixels. Common examples of raster data include satellite imagery, elevation models, and land use classifications. 

In rasters, the color of each pixel is its value: for example, an elevation map may use a grayscale color scheme where white represents the highest points, black represents the lowest, and varying shades of gray are used in between.

In addition to the data you place on the map, most maps also include a **basemap**, or a backround layer that serves as a helpful visual reference for your audience.

---

## Projections

One of the most fundamental problems in geography is that the earth is a sphere, but maps are flat. To visualize why this causes a problem, imagine peeling an orange and flattening the peel out on the table. The (more or less) spherical orange peel will tear in some places and condense in others in order to conform with the flat surface. It's the same with maps: cartographers have devised many different projection systems, or rules according to which the shape of the earth is translated to a flat surface. Some maintain area of landmasses at the expense of shape, direction, and distance, while others prioritize another of those properties. 

For practical purposes: the tools we'll be using today, ArcGIS Online and Leaflet, use the Web Mercator projection. This projection is very good at showing accurate shapes at the local level, but in a global view it significantly distorts and enlarges shapes closer to the poles. All projections have their pros and cons, and Web Mercator is the standard for web mapping for a reason, but it's important to recognize its weak points. 

**Quick activity:** visit [The True Size of...](https://thetruesize.com/){:target="_blank" rel="noopener"}. Enter a state or country into the search bar, then click and drag its shape north and south to see how it would look in Web Mercator if it were located in a different part of the world.

You can change the projection you use in ArcGIS Online, but you shouldn't unless it's for a specific, good reason. 

---

## How (not) to lie with maps

A map is a representation of specific information about a specific part of the world. It's important to keep that in mind: it's a _representation,_ not an objective, complete picture. Map creators must make decisions about what data is included, what data is excluded, and how it's all displayed. 

It's easy to make a bad map. Poor color choices, too much (or to little) data, and improper classification of data can confuse or mislead (intentionally or unintentionally). 

When making a map, continually ask yourself these questions, and use your answers to continuously improve:
- What am I trying to argue?
- Does the data displayed on the map make that argument well?
- Does my color scheme enhance or detract from my argument?
- Could my argument be misunderstood?

---

## GIS and Web Mapping Tools

Tools for geospatial analysis fall into two broad categories.

**Desktop GIS apps** are best when you need to do complex analysis and data processing.
- [ArcGIS Pro](https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview){:target="_blank" rel="noopener"}: The industry standard. Proprietary, but free for ISU students through the [ISU GIS Facility.](https://www.gis.iastate.edu/services/software/arcgis-pro-installation-and-licensing/){:target="_blank" rel="noopener"}
- [QGIS](https://qgis.org/){:target="_blank" rel="noopener"}: A free and open source alternative to ArcGIS Pro.

**Web mapping tools** are best for creating, publishing, and sharing interactive maps.
- [ArcGIS Online](https://www.arcgis.com){:target="_blank" rel="noopener"}: The most feature-rich web-mapping platform. ISU students have free accounts through the [ISU GIS Facility.](isugisf.maps.arcgis.com){:target="_blank" rel="noopener"}
- [Leaflet](https://leafletjs.com/){:target="_blank" rel="noopener"}: lightweight JavaScript library for creating maps.

---

## What we'll be building today

For the rest of this session, I'll demo two tools and then you'll get hands-on experience building maps with them. 

**Activity 1: ArcGIS Online Map Viewer**
Find pre-existing data (and create your own), style it on a map, and publish it to ArcGIS Online.

**Activity 2: Leaflet (with a template)**
Using a pre-made GitHub template, create a simple, interactive map with Leaflet and host it on a GitHub Pages site.