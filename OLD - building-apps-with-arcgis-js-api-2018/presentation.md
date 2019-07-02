
<!-- .slide: data-background="../images/bg-1.png" -->

## Building <span style="color:#D9BA6F">3D</span> Apps <br/> with ArcGIS API for JavaScript

<p>Veronika Landers - Yannik Messerli - Johannes Schmid</p>

---

<!-- .slide: data-background="../images/bg-2.png" -->

### <b> <span style="color:#D9BA6F">3D</span> GIS across industries</b>

<br/>

<div class="box" style="display:inline-block; width:650px">
<iframe id="scene-view-map-view" data-src="https://www.arcgis.com/home/webscene/viewer.html?webscene=c5b58fa63714412eb0eea933a130ebdf&ui=min" align=left></iframe></div>
<div class="box" style="display:inline-block; width:50px"></div>
<div class="box" style="display:inline-block; width:650px">
<iframe id="scene-view-map-view" data-src="https://www.arcgis.com/home/webscene/viewer.html?webscene=43e1b988e55a44fdad6c5cf58c34dbda&ui=min"></iframe></div>

---

<!-- .slide: data-background="../images/bg-1.png" -->
### <b>Agenda</b>

- Introduction
- Your first 3D app
- Working with the API
- Demos

---

<!-- .slide: data-background="../images/bg-4.png" -->

## <b>Introduction</b>

<br/>

<p>Veronika Landers</p>

---

<!-- .slide: data-background="../images/bg-2.png" -->

### <b>The ArcGIS Platform</b>


<img class="plain" src="./images/platform.png" height=500 background=none>

---

<!-- .slide: data-background="../images/bg-2.png" -->

### <b>The ArcGIS <span style="color:#D9BA6F">3D</span> Platform</b>


<img class="plain" src="./images/platform-3d.png" height=500 background=none>

---

<!-- .slide: data-background="../images/bg-2.png" -->

### <b>Out-of-the-box <span style="color:#D9BA6F">3D</span> Web Apps</b>


<img class="plain" src="./images/appsamples.png" height=500 background=none>

---

<!-- .slide: data-background="../images/bg-2.png" -->

### <b>Building Apps with the ArcGIS <span style="color:#D9BA6F">3D</span> Platform</b>


<img class="plain" src="./images/platform-3d-js.png" height=500 background=none>

---

<!-- .slide: data-background="../images/bg-2.png" -->

### <b>Custom <span style="color:#D9BA6F">3D</span> Web Apps</b>


<img class="plain" src="./images/customsamples.png" height=500 background=none>

---

<!-- .slide: data-background="../images/bg-2.png" -->
### <b>ArcGIS API for JavaScript</b>

<br/>
<img class="plain" src="./images/js-doc.png" height=500 background=none>

---

<!-- .slide: data-background="../images/bg-2.png" -->
### <b>ArcGIS API for JavaScript </b>

  - Visual mapping (2D & 3D), components and widgets
  - Support for various different layer types (data sources)
  - Integration with the ArcGIS platform
    <br/>(security, sign-in, premium services, …)

<br/>

<b><span style="color:#D9BA6F">Get it today</span></b>

Find doc & samples to get started at https://developers.arcgis.com/javascript

---

<!-- .slide: data-background="../images/bg-2.png" -->

### <b>Desktop <span style="color:#D9BA6F">3D</span> Requirements</b>

<br/>

- Modern hardware, especially Graphics Card

- Latest web browsers with WebGL support
  - Chrome
  - Edge / Internet Explorer 11\* (\*WebGL not optimized)
  - Firefox
  - Safari

---

<!-- .slide: data-background="../images/bg-2.png" -->


### <b>Mobile <span style="color:#D9BA6F">3D</span> Requirements</b>

<br/>

- Mobile support introduced this year!
- Officially supported for the following devices
  - iOS — iPhone 8, iPad Pro (Safari)
  - Android — Samsung S8/S9 (Chrome)
  - Android - Samsung Tab S3 (Chrome)

- Other devices *only at your own risk* :)

---

<!-- .slide: data-background="../images/bg-2.png" -->

### <b>Content for your apps</b>

<img class="plain" src="./images/publish.png" height=600 background=none>

---

<!-- .slide: data-background="../images/bg-2.png" -->

### <b>Publish a layer in ArcGIS Pro</b>

<img class="plain" src="./images/publish-pro-layer.png" height=700 background=none>

---

<!-- .slide: data-background="../images/bg-2.png" -->

### <b>Publish a web scene in ArcGIS Pro</b>

<img class="plain" src="./images/publish-pro.png" height=700 background=none>

---

<!-- .slide: data-background="../images/bg-2.png" -->

### <b>Coordinate System Support for Scenes</b>

- Each scene has its coordinate system defined.
- Cached data needs to be provided in the defined system.
- Feature and dynamic data is projected on the fly.
- Coordinate systems define the type of scenes and its capabilities.

---

<!-- .slide: data-background="../images/bg-2.png" -->

### <b>Global scenes</b>

Visualize data on a full globe

<img class="plain" src="./images/globalscene.png" height=500 background=none>

---

<!-- .slide: data-background="../images/bg-2.png" -->

### <b>Global scenes</b>

Choose one of two geographic coordinate systems
  - WebMercator (wkid: 3857) - ideal to use Esri provided cached data
  - WGS84 (wkid: 4326)

---

<!-- .slide: data-background="../images/bg-2.png" -->

### <b>Local scenes</b>

Visualize data in a local planar way
  
<img class="plain" src="./images/localscene.png" height=500 background=none>


---

<!-- .slide: data-background="../images/bg-2.png" -->

### <b>Local scenes</b>

Choose one of the following options
- WebMercator (wkid: 3857)
- any projected coordinate system

Clip to your area of interest

---

<!-- .slide: data-background="../images/bg-2.png" -->

### <b>Web Scenes Concept</b>

- Vehicle for cross platform 3D capabilities
- Collection of layers, environment settings, slides
- Read and write Web Scenes across the ArcGIS platform

<img class="plain" src="./images/platform-webscene.png" background=none>


---

<!-- .slide: data-background="../images/bg-4.png" -->

## <b>Your first 3D App</b>

<br/>

<div style="margin-top: -70px; font-size: 80%; font-style: italic;">with the ArcGIS API for JavaScript</div>

<br/>

<p>Yannik Messerli</p>

---

<!-- .slide: data-background="../images/bg-5.png" -->

### Steps

1. Loading the webscene
1. Add a layer
1. Add a widget
1. Configure popups

---

<!-- .slide: data-background="../images/bg-6.png" -->

## Creating basic HTML file

<div class="code-snippet" style="max-width: 600px; font-size: 130%; float: none; margin: auto;">
    <pre><code style="margin-bottom: -30px;" class="lang-html">
    &lt;!DOCTYPE html&gt;
    &lt;html&gt;
    &lt;head&gt;
      &lt;meta charset=&quot;utf-8&quot;&gt;
    </code>
    <code style="margin-bottom: -30px;" class="grey">
      &lt;link rel=&quot;stylesheet&quot; href=&quot;//js.arcgis.com/4.8/esri/css/main.css&quot;&gt;
      &lt;script src=&quot;//js.arcgis.com/4.8/&quot;&gt;&lt;/script&gt;
    </code>
    <code style="margin-bottom: -30px;" class="lang-html">
      &lt;title&gt;Create a 3D map&lt;/title&gt;
    &lt;/head&gt;
    &lt;body&gt;
      &lt;script&gt;
    </code>
    <code style="margin-bottom: -30px;" class="grey">
        require([
          "esri/WebScene",
          "esri/views/SceneView",
          "dojo/domReady!"
        ], function(WebScene, SceneView) {
          var scene = new WebScene({
            portalItem: {
              id: "e5dab9bfc78a46d08276b185026fc20a"
            }
          });
          var view = new SceneView({
            container: "viewDiv",
            map: scene
          });
        });
    </code>
    <code class="lang-html">
      &lt;/script&gt;
      &lt;div id=&quot;viewDiv&quot;&gt;&lt;/div&gt;
    &lt;/body&gt;
    &lt;/html&gt;
    </code></pre>
    </div>


---

<!-- .slide: data-background="../images/bg-6.png" -->

## Reference the ArcGIS API for JavaScript

<div class="code-snippet" style="max-width: 600px; font-size: 130%; float: none; margin: auto;">
    <pre><code style="margin-bottom: -30px;" class="grey">
    &lt;!DOCTYPE html&gt;
    &lt;html&gt;
    &lt;head&gt;
      &lt;meta charset=&quot;utf-8&quot;&gt;
    </code>
    <code style="margin-bottom: -30px;" class="lang-html">
      &lt;link rel=&quot;stylesheet&quot; href=&quot;//js.arcgis.com/4.8/esri/css/main.css&quot;&gt;
      &lt;script src=&quot;//js.arcgis.com/4.8/&quot;&gt;&lt;/script&gt;
    </code>
    <code style="margin-bottom: -30px;" class="grey">
      &lt;title&gt;Create a 3D map&lt;/title&gt;
    &lt;/head&gt;
    &lt;body&gt;
      &lt;script&gt;
    </code>
    <code style="margin-bottom: -30px;" class="grey">
        require([
          "esri/WebScene",
          "esri/views/SceneView",
          "dojo/domReady!"
        ], function(WebScene, SceneView) {
          var scene = new WebScene({
            portalItem: {
              id: "e5dab9bfc78a46d08276b185026fc20a"
            }
          });
          var view = new SceneView({
            container: "viewDiv",
            map: scene
          });
        });
    </code>
    <code class="grey">
      &lt;/script&gt;
      &lt;div id=&quot;viewDiv&quot;&gt;&lt;/div&gt;
    &lt;/body&gt;
    &lt;/html&gt;
    </code></pre>
    </div>


---

<!-- .slide: data-background="../images/bg-6.png" -->

## Load the module

<div class="code-snippet" style="max-width: 600px; font-size: 130%; float: none; margin: auto;">
    <pre><code style="margin-bottom: -30px;" class="grey">
    &lt;!DOCTYPE html&gt;
    &lt;html&gt;
    &lt;head&gt;
      &lt;meta charset=&quot;utf-8&quot;&gt;
    </code>
    <code style="margin-bottom: -30px;" class="grey">
      &lt;link rel=&quot;stylesheet&quot; href=&quot;//js.arcgis.com/4.8/esri/css/main.css&quot;&gt;
      &lt;script src=&quot;//js.arcgis.com/4.8/&quot;&gt;&lt;/script&gt;
    </code>
    <code style="margin-bottom: -30px;" class="grey">
      &lt;title&gt;Create a 3D map&lt;/title&gt;
    &lt;/head&gt;
    &lt;body&gt;
      &lt;script&gt;
    </code>
    <code style="margin-bottom: -30px;" class="lang-js">
        require([
          "esri/WebScene",
          "esri/views/SceneView",
          "dojo/domReady!"
        ], function(WebScene, SceneView) {
    </code>
    <code style="margin-bottom: -30px;" class="grey">
          var scene = new WebScene({
            portalItem: {
              id: "e5dab9bfc78a46d08276b185026fc20a"
            }
          });
          var view = new SceneView({
            container: "viewDiv",
            map: scene
          });
    </code>
    <code style="margin-bottom: -30px;" class="lang-js">
        });
    </code>
    <code class="grey">
      &lt;/script&gt;
      &lt;div id=&quot;viewDiv&quot;&gt;&lt;/div&gt;
    &lt;/body&gt;
    &lt;/html&gt;
    </code></pre>
    </div>


---

<!-- .slide: data-background="../images/bg-6.png" -->

## Instantiate the webscene

<div class="code-snippet" style="max-width: 600px; font-size: 130%; float: none; margin: auto;">
    <pre><code style="margin-bottom: -30px;" class="grey">
    &lt;!DOCTYPE html&gt;
    &lt;html&gt;
    &lt;head&gt;
      &lt;meta charset=&quot;utf-8&quot;&gt;
    </code>
    <code style="margin-bottom: -30px;" class="grey">
      &lt;link rel=&quot;stylesheet&quot; href=&quot;//js.arcgis.com/4.8/esri/css/main.css&quot;&gt;
      &lt;script src=&quot;//js.arcgis.com/4.8/&quot;&gt;&lt;/script&gt;
    </code>
    <code style="margin-bottom: -30px;" class="grey">
      &lt;title&gt;Create a 3D map&lt;/title&gt;
    &lt;/head&gt;
    &lt;body&gt;
      &lt;script&gt;
    </code>
    <code style="margin-bottom: -30px;" class="grey">
        require([
          "esri/WebScene",
          "esri/views/SceneView",
          "dojo/domReady!"
        ], function(WebScene, SceneView) {
    </code>
    <code style="margin-bottom: -30px;" class="lang-js">
          var scene = new WebScene({
            portalItem: {
              id: "e5dab9bfc78a46d08276b185026fc20a"
            }
          });
    </code>
    <code style="margin-bottom: -30px;" class="grey">
          var view = new SceneView({
            container: "viewDiv",
            map: scene
          });
        });
    </code>
    <code class="grey">
      &lt;/script&gt;
      &lt;div id=&quot;viewDiv&quot;&gt;&lt;/div&gt;
    &lt;/body&gt;
    &lt;/html&gt;
    </code></pre>
</div>
<p class="fragment" data-fragment-index="1" style="position: absolute; top: 100px; max-width: 800px; margin-left: -50%; left: 75%;">
  <img src="./images/portalitem.png" alt="">
</p>

---

<!-- .slide: data-background="../images/bg-6.png" -->

## Create the view

<div class="code-snippet" style="max-width: 600px; font-size: 130%; float: none; margin: auto;">
    <pre><code style="margin-bottom: -30px;" class="grey">
    &lt;!DOCTYPE html&gt;
    &lt;html&gt;
    &lt;head&gt;
      &lt;meta charset=&quot;utf-8&quot;&gt;
    </code>
    <code style="margin-bottom: -30px;" class="grey">
      &lt;link rel=&quot;stylesheet&quot; href=&quot;//js.arcgis.com/4.8/esri/css/main.css&quot;&gt;
      &lt;script src=&quot;//js.arcgis.com/4.8/&quot;&gt;&lt;/script&gt;
    </code>
    <code style="margin-bottom: -30px;" class="grey">
      &lt;title&gt;Create a 3D map&lt;/title&gt;
    &lt;/head&gt;
    &lt;body&gt;
      &lt;script&gt;
    </code>
    <code style="margin-bottom: -30px;" class="grey">
        require([
          "esri/WebScene",
          "esri/views/SceneView",
          "dojo/domReady!"
        ], function(WebScene, SceneView) {
    </code>
    <code style="margin-bottom: -30px;" class="grey">
          var scene = new WebScene({
            portalItem: {
              id: "e5dab9bfc78a46d08276b185026fc20a"
            }
          });
    </code>
    <code style="margin-bottom: -30px;" class="lang-js">
          var view = new SceneView({
            container: "viewDiv",
            map: scene
          });
    </code>
    <code class="grey">
        });
      &lt;/script&gt;
      &lt;div id=&quot;viewDiv&quot;&gt;&lt;/div&gt;
    &lt;/body&gt;
    &lt;/html&gt;
    </code></pre>
    </div>


---

<!-- .slide: data-background="../images/bg-6.png" -->

## Your first 3D app!

<div class="two-columns">
  <div class="left-column">

<div class="code-snippet">
    <pre><code style="margin-bottom: -30px;" class="lang-html">
    &lt;!DOCTYPE html&gt;
    &lt;html&gt;
    &lt;head&gt;
      &lt;meta charset=&quot;utf-8&quot;&gt;
    </code>
    <code style="margin-bottom: -30px;" class="lang-html">
      &lt;link rel=&quot;stylesheet&quot; href=&quot;//js.arcgis.com/4.8/esri/css/main.css&quot;&gt;
      &lt;script src=&quot;//js.arcgis.com/4.8/&quot;&gt;&lt;/script&gt;
    </code>
    <code style="margin-bottom: -30px;" class="lang-html">
      &lt;title&gt;Create a 3D map&lt;/title&gt;
    &lt;/head&gt;
    &lt;body&gt;
      &lt;script&gt;
    </code>
    <code style="margin-bottom: -30px;" class="lang-js">
        require([
          "esri/WebScene",
          "esri/views/SceneView",
          "dojo/domReady!"
        ], function(WebScene, SceneView) {
          var scene = new WebScene({
            portalItem: {
              id: "e5dab9bfc78a46d08276b185026fc20a"
            }
          });
          var view = new SceneView({
            container: "viewDiv",
            map: scene
          });
        });
    </code>
    <code class="lang-html">
      &lt;/script&gt;
      &lt;div id=&quot;viewDiv&quot;&gt;&lt;/div&gt;
    &lt;/body&gt;
    &lt;/html&gt;
    </code></pre>
    </div>


  </div>
  <div class="right-column">
    <iframe id="scene-view-map-view" data-src="./snippets/setup-snippet-1.html" ></iframe>
  </div>
</div>

---

<!-- .slide: data-background="../images/bg-4.png" -->

## Details about the `Webscene` class

- `Layers`, `Presentation`, ...
- `Basemap` is exactly the same concept as in 2D
- `Ground` defines the ground surface of the scene

---

<!-- .slide: data-background="../images/bg-8.png" -->

## Layers

|              |  |
|--------------|--|
| `FeatureLayer` | <small>2D & 3D</small> |
| `CSVLayer` | <small>2D & 3D</small> |
| `StreamLayer` | <small>2D & 3D</small> |
| `MapImageLayer` | <small>2D & 3D</small> |
| `ImageryLayer` | <small>2D & 3D</small> |
| `WMSLayer` | <small>2D & 3D</small> |
| `OpenStreetMapLayer` | <small>2D & 3D</small> |
| `TileLayer` | <small>2D & 3D</small> |
| `WebTileLayer` | <small>2D & 3D</small> |
| `WMTSLayer` | <small>2D & 3D</small> |
| `VectorTileLayer` | <small>2D & 3D</small> |
| `ElevationLayer` | <small> 3D only</small> |
| `SceneLayer` | <small> 3D only</small> |
| `IntegratedMeshLayer` | <small> 3D only</small> |
| `PointCloudLayer` | <small> 3D only</small> |

---

<!-- .slide: data-background="../images/bg-8.png" -->

## Layers

|              |  |
|--------------|--|
| <div style="font-size: 300%; background: rgba(27, 75, 127, 0.55); position: absolute;">`FeatureLayer`</div> | <small>2D & 3D</small> |
| `CSVLayer` | <small>2D & 3D</small> |
| `StreamLayer` | <small>2D & 3D</small> |
| `MapImageLayer` | <small>2D & 3D</small> |
| `ImageryLayer` | <small>2D & 3D</small> |
| `WMSLayer` | <small>2D & 3D</small> |
| `OpenStreetMapLayer` | <small>2D & 3D</small> |
| `TileLayer` | <small>2D & 3D</small> |
| `WebTileLayer` | <small>2D & 3D</small> |
| `WMTSLayer` | <small>2D & 3D</small> |
| `VectorTileLayer` | <small>2D & 3D</small> |
| `ElevationLayer` | <small> 3D only</small> |
| `SceneLayer` | <small> 3D only</small> |
| `IntegratedMeshLayer` | <small> 3D only</small> |
| `PointCloudLayer` | <small> 3D only</small> |

---

<!-- .slide: data-background="../images/bg-4.png" -->

## Adding a layer

<div class="code-snippet" style="font-size: 140%; max-width: 600px; float: none; margin: auto;">
    <pre><code style="margin-bottom: -40px;" class="grey">
        require([
          "esri/WebScene",
          "esri/views/SceneView",
    </code>
    <code style="margin-bottom: -40px;" class="lang-js">
          "esri/layers/FeatureLayer",
    </code>
    <code style="margin-bottom: -40px;" class="grey">
          "dojo/domReady!"
    </code>
    <code style="margin-bottom: -40px;" class="lang-js">
        ], function(WebScene, SceneView, FeatureLayer) {
    </code>
    <code style="margin-bottom: -40px;" class="grey">
          var scene = new WebScene({
            portalItem: {
              id: "e5dab9bfc78a46d08276b185026fc20a"
            }
          });
          var view = new SceneView({
            container: "viewDiv",
            map: scene
          });
    </code>
    <code style="margin-bottom: -40px;" class="lang-js">
          var layer = new FeatureLayer({
            portalItem: {
              id: "a38c0bd41aad41d89ab2a31050ff07b1"
            }
          });
          scene.add(layer);
    </code>
    <code class="grey">
        });
    </code></pre>
    </div>

---

<!-- .slide: data-background="../images/bg-4.png" -->

## Adding a layer

<div class="two-columns">
  <div class="left-column">

<div class="code-snippet" style="font-size: 140%;">
    <pre><code class="lang-js">
        require([
          "esri/WebScene",
          "esri/views/SceneView",
          "esri/layers/FeatureLayer",
          "dojo/domReady!"
        ], function(WebScene, SceneView, FeatureLayer) {
          var scene = new WebScene({
            portalItem: {
              id: "e5dab9bfc78a46d08276b185026fc20a"
            }
          });
          var view = new SceneView({
            container: "viewDiv",
            map: scene
          });
          var layer = new FeatureLayer({
            portalItem: {
              id: "a38c0bd41aad41d89ab2a31050ff07b1"
            }
          });
          scene.add(layer);
        });
    </code></pre>
    </div>


  </div>
  <div class="right-column">
    <iframe id="scene-view-map-view" data-src="./snippets/setup-snippet-2.html"></iframe>
  </div>
</div>


---

<!-- .slide: data-background="../images/bg-7.png" -->

## Widgets

<div style="max-width:70%;margin: auto; margin-bottom: 50px;">Widgets are UI components that add functionalities to your scene.  The API provides ready-to-use widgets, for example:</div>

- `Legend`
- `LayerList`
- `Search`
- ...


---

<!-- .slide: data-background="../images/bg-7.png" -->

## Adding a widget


<div class="code-snippet" style="font-size: 140%;max-width: 600px; float: none; margin: auto;">
    <pre><code style="margin-bottom: -40px;" class="grey">
        require([
          "esri/WebScene",
          "esri/views/SceneView",
          "esri/layers/FeatureLayer",
    </code>
    <code style="margin-bottom: -40px;" class="lang-js">
          "esri/widgets/Search",
    </code>
    <code style="margin-bottom: -40px;" class="grey">
          "dojo/domReady!"
        ], function(
          WebScene, 
          SceneView, 
          FeatureLayer,
    </code>
    <code style="margin-bottom: -40px;" class="lang-js">
          Search
        ) {
    </code>
    <code style="margin-bottom: -40px;" class="grey">

          // ...

    </code>
    <code style="margin-bottom: -40px;" class="lang-js">
          var searchWidget = new Search({
            view: view
          });
          view.ui.add(searchWidget, {
            position: "top-right"
          });
    </code>
    <code class="grey">
        });
    </code></pre>
    </div>


---

<!-- .slide: data-background="../images/bg-7.png" -->

## Adding a widget

<div class="two-columns">
  <div class="left-column">

<div class="code-snippet" style="font-size: 140%;">
    <pre><code class="lang-js">
        require([
          "esri/WebScene",
          "esri/views/SceneView",
          "esri/layers/FeatureLayer",
          "esri/widgets/Search",
          "dojo/domReady!"
        ], function(
          WebScene, 
          SceneView, 
          FeatureLayer,
          Search
        ) {

          // ...

          var searchWidget = new Search({
            view: view
          });
          view.ui.add(searchWidget, {
            position: "top-right"
          });
        });
    </code></pre>
    </div>


  </div>
  <div class="right-column">
    <iframe id="scene-view-map-view" data-src="./snippets/setup-snippet-3.html"></iframe>
  </div>
</div>

---

<!-- .slide: data-background="../images/bg-7.png" -->

## Popups

<div class="two-columns">
  <div class="left-column">
<div>Enable on a layer:</div>
  <div class="code-snippet" style="font-size: 120%;margin-top: 20px;">
    <pre><code class="lang-js" style="margin-bottom: 20px;">
  layer.popupEnabled = true;
</code></pre></div>

<br><br>
<div>
Open it programmatically:
</div>
      <div class="code-snippet" style="font-size: 120%;margin-top: 30px;">
        <pre><code class="lang-js">
  view.on("click", function(event) {
    event.stopPropagation();
    view.popup.open({
      title: "Reverse geocode: [" 
        + event.mapPoint.longitude 
        + ", " + event.mapPoint.latitude 
        + "]",
      location: event.mapPoint
    });
  });
        </code></pre>
      </div>

  </div>
  <div class="right-column">
    <iframe id="scene-view-map-view" data-src="./snippets/setup-snippet-3.html"></iframe>
  </div>
</div>

---

<!-- .slide: data-background="../images/bg-7.png" -->

## Popup templates

<div class="two-columns">
  <div class="left-column">
    Display attribute using the `PopupTemplate`
    <div class="code-snippet" style="font-size: 130%;">
      <pre><code class="lang-js">
  var template = {
    title: "Building <b>{NAME}</b>",
    content: "This build has an enery consumption<br/>"
      + "of <b>{ElectricUse}</b> kBTU, for a score "
      + "of <b>{StarScore}</b>."
  };
  layer.popupTemplate = template;
      </code></pre>
    </div>
  </div>
  <div class="right-column">
    <iframe id="scene-view-map-view" data-src="./snippets/setup-snippet-4.html"></iframe>
  </div>
</div>

---

<!-- .slide: data-background="../images/bg-4.png" -->

## <b>Working with the API</b>


<br/>

<p>Johannes Schmid</p>

---

<!-- .slide: data-background="../images/bg-4.png" -->

## Architecture
<br/>
<img src="../images/concepts-architecture2.png" width="60%" style="border: none; background: none; box-shadow: none"/>

---

## Architecture
<br/>
<img src="../images/concepts-architecture3.png" width="60%" style="border: none; background: none; box-shadow: none"/>

---

<!-- .slide: data-background="../images/bg-4.png" -->

## Working with the [SceneView](https://developers.arcgis.com/javascript/latest/api-reference/esri-views-SceneView.html)

<div class="code-snippet" style="font-size: 160%;">
  <pre><code class="lang-ts">
class SceneView {
  // Camera specifies the view
  camera: Camera;

  // Animations, framing
  goTo(...);

  // Finding graphics at screen locations
  hitTest(...);

  // Converting coordinate systems
  toScreen(mapPoint: Point): ScreenPoint;
  toMap(screenPoint: ScreenPoint): Point;
}
  </code></pre>
</div>

---

<!-- .slide: data-background="../images/bg-4.png" -->

## [Camera](https://developers.arcgis.com/javascript/latest/api-reference/esri-Camera.html)

- Primary specification of the view is the [`Camera`](https://developers.arcgis.com/javascript/beta/api-reference/esri-Camera.html)


<div class="code-snippet" style="font-size: 160%;">
  <pre><code class="lang-ts">
class Camera {
  // The position of the camera eye in 3D space (x, y + z elevation)
  position: Point;

  // The heading angle (towards north in degrees, [0, 360]°)
  heading: number;

  // The tilt angle ([0, 180]°, with 0° straight down, 90° horizontal)
  tilt: number;
}
  </code></pre>
</div>

---

<!-- .slide: data-background="../images/bg-4.png" -->

## [Camera](https://developers.arcgis.com/javascript/latest/api-reference/esri-Camera.html)

<div class="two-columns">
  <div class="left-column">

<div class="code-snippet" style="font-size: 160%;">
<button class="play" id="scene-view-camera-button01"></button>
<pre><code class="lang-ts">const camera = view.camera.clone();

// Increment the heading of the camera by 5 degrees
camera.heading += 5;

// Set the modified camera on the view
view.camera = camera;</code></pre>
</div>


  </div>
  <div class="right-column">
    <iframe id="camera-demo" data-src="./snippets/concepts-camera.html" ></iframe>
  </div>
</div>

---

<!-- .slide: data-background="../images/bg-4.png" -->

## [goTo](https://developers.arcgis.com/javascript/latest/api-reference/esri-views-SceneView.html#goTo)

<div class="two-columns">
  <div class="left-column">

<div class="code-snippet" style="font-size: 160%;">
<button class="play" id="scene-view-go-to-button01"></button>
<pre><code class="lang-ts">// target heading = current heading + 30
var newHeading = view.camera.heading + 30;

// go to heading preserves view.center
view.goTo({
    heading: newHeading
});</code></pre>
</div>

<div class="code-snippet" style="font-size: 160%;">
<button class="play" id="scene-view-go-to-button02"></button>
<pre><code class="lang-ts">// coordinates (lon, lat) of Mount Fuji
var newCenter = [138.729050, 35.360638];

view.goTo({
   center: newCenter,
   zoom: 13
});</code></pre>
</div>

  </div>
  <div class="right-column">
    <iframe id="go-to-demo" data-src="./snippets/concepts-goTo.html" ></iframe>
  </div>
</div>

---

<!-- .slide: data-background="../images/bg-4.png" -->

## [toMap](https://developers.arcgis.com/javascript/latest/api-reference/esri-views-SceneView.html#toMap)

<div class="two-columns">
  <div class="left-column">

<div class="code-snippet small" style="font-size: 160%;">
<pre><code class="lang-js">// Every time the user clicks on the map...
view.on("click", function(event) {

  // convert the screen position to map coordinates
  var position = view.toMap(event.x, event.y);
  
  // add a cone symbol at that location
  view.graphics.add(new Graphic({
    geometry: position,
    symbol: coneSymbol
  });
});</code></pre>
</div>

  </div>
  <div class="right-column">
    <iframe id="to-map-to-screen-demo" data-src="./snippets/concepts-toMap.html" ></iframe>
  </div>
</div>

---

<!-- .slide: data-background="../images/bg-4.png" -->

## Working with layers

<div class="code-snippet" style="font-size: 160%;">
  <pre><code class="lang-ts">
class SceneLayer {
  // Filtering 
  definitionExpression: string;

  // Renderer assigns each feature a color and style
  renderer: Renderer;

  // Querying
  queryFeatures(params: Query): FeatureSet;
  queryExtent(params: Query): Extent;
  ...
}
  </code></pre>
</div>

---

<!-- .slide: data-background="../images/bg-4.png" -->

## Filtering

<div class="two-columns">
  <div class="left-column">
<div class="code-snippet" style="font-size: 160%;">
<button class="play" id="mesh-filtering-button01"></button>
<pre><code class="lang-js">// only show buildings constructed before 1900
sceneLayer.definitionExpression =
  "CNSTRCT_YR < 1900 AND CNSTRCT_YR > 0";
</code></pre>
</div>

<div class="code-snippet" style="font-size: 160%;">
<button class="play" id="mesh-filtering-button03"></button>
<pre><code class="lang-js">// reset filter
sceneLayer.definitionExpression = null;
</code></pre>
</div>

<div class="code-snippet" style="font-size: 160%;">
<button class="play" id="mesh-filtering-button02"></button>
<pre><code class="lang-js">// only show tall buildings
sceneLayer.definitionExpression =
  "HEIGHTROOF > 300";
</code></pre>
</div>

  </div>
  <div class="right-column">
    <iframe id="scene-layer-mesh2" data-src="./snippets/concepts-definitionExpression.html" ></iframe>
  </div>
</div>

---

<!-- .slide: data-background="../images/bg-4.png" -->

## Setting layer style

<div class="two-columns">
  <div class="left-column">
<div class="code-snippet" style="font-size: 130%;">
<button class="play" id="mesh-renderer-button01"></button>
<pre><code class="lang-js">// draw buildings in transparent green
sceneLayer.renderer = {
  type: "simple",
  symbol: {
    type: "mesh-3d",
    symbolLayers: [{
      type: "fill",
      material: {
        color: [144, 238, 144, 0.3]
      }
    }]
  }
};
</code></pre>
</div>

<div class="code-snippet" style="font-size: 130%;">
<button class="play" id="mesh-renderer-button02"></button>
<pre><code class="lang-js">// color buildings by construction year
sceneLayer.renderer = {
 type: "simple",
 visualVariables: [{
   type: "color",
   field: "CNSTRCT_YR",
   stops: [{
       value: 1867,
       color: [69, 83, 122]
     },
     ...
   ]
 }]
};
</code></pre>
</div>

  </div>
  <div class="right-column">
    <iframe id="scene-layer-mesh2" data-src="./snippets/concepts-renderer.html" ></iframe>
  </div>
</div>

---

<!-- .slide: data-background="../images/bg-4.png" -->

### ArcGIS API for JavaScript: 3D Visualization
Thursday, 10:00 am - 11:00 am<br/>
Room 33C

---

## [Underground](https://developers.arcgis.com/javascript/latest/api-reference/esri-Ground.html)

<div class="two-columns">
  <div class="left-column">
<div class="code-snippet" style="font-size: 130%;">
<button class="play" id="underground-button01"></button>
<pre><code class="lang-js">// Ground object is part of Map/WebScene
var ground = webScene.ground;

// Set ground to 50% transparent
ground.opacity = 0.5;
</code></pre>
</div>

<div class="code-snippet" style="font-size: 130%;">
<button class="play" id="underground-button02"></button>
<pre><code class="lang-js">// allow camera to go underground
ground.navigationConstraint = {
  type: "none"
};
</code></pre>
</div>

  </div>
  <div class="right-column">
    <iframe id="scene-layer-mesh2" data-src="./snippets/concepts-underground.html" ></iframe>
  </div>
</div>

---

<!-- .slide: data-background="../images/bg-4.png" -->

### There is so much more...

[https://developers.arcgis.com/javascript/](https://developers.arcgis.com/javascript/)

<img src="../images/api-doc.png" height="500"/>

---

<!-- .slide: data-background="../images/bg-4.png" -->

<h3>ArcGIS API for JavaScript: An Introduction</h3>
Tuesday, 4:00 pm - 5:00 pm<br/>
Room 30E<br/>
<br/>
<br/>

<h3 class="fragment" data-fragment-index="1">ArcGIS API for JavaScript: Best Practices for Building Apps</h3>
<span class="fragment" data-fragment-index="1">Wednesday, 2:30 pm - 3:30 pm<br/>
Room 31A<br/>
</span>

---

<!-- .slide: data-background="../images/bg-1.png" -->

## <b>Demos</b> 

<br/>

<div style="margin-top: -70px; font-size: 80%; font-style: italic;">of 3D applications</div>

<br/>

<p>Veronika Landers - Johannes Schmid - Yannik Messerli</p>

---

<!-- .slide: data-background="../images/bg-4.png" -->

### Related sessions
<br/>

**ArcGIS API for JavaScript: An Introduction**<br/>
Tuesday, 4:00 pm - 5:00 pm<br/>
Room 30E<br/>

**ArcGIS API for JavaScript: Best Practices for Building Apps**<br/>
Wednesday, 2:30 pm - 3:30 pm<br/>
Room 31A<br/>

**ArcGIS API for JavaScript: 3D Visualization**<br/>
Thursday, 10:00 am - 11:00 am<br/>
Room 33C

---

<!-- .slide: data-background="../images/bg-2.png" -->

### Please Take Our Survey on the App

<img class="plain" src="./images/survey.png" background=none>

---

<!-- .slide: data-background="../images/bg-5.png" -->

### Topics


- [Skyscraper explorer](https://esri.github.io/Manhattan-skyscraper-explorer/)
- [Hiking App](https://ralucanicola.github.io/hiking-app/)
- [C-Through](https://esri.github.io/c-through/)
- [Satellite map](https://richiecarmichael.github.io/sat/index.html)
- [Landsat viewer](https://richiecarmichael.github.io/landsat-viewer/index.html)

---

<!-- .slide: data-background="../images/bg-8.png" -->

<img class="plain" src="../images/esri-science-logo-white.png" background=none>

---

<!-- .slide: data-background="../images/bg-5.png" -->


### Skyscraper explorer

<iframe id="scene-view-map-view" data-src="https://esri.github.io/Manhattan-skyscraper-explorer/"></iframe>

---

<!-- .slide: data-background="../images/bg-5.png" -->

### Hiking App

<iframe id="scene-view-map-view" data-src="https://ralucanicola.github.io/hiking-app/"></iframe>

---

<!-- .slide: data-background="../images/bg-5.png" -->

### C-Through

<iframe id="scene-view-map-view" data-src="https://esri.github.io/c-through/"></iframe>

---

<!-- .slide: data-background="../images/bg-5.png" -->

### Satellite map

<iframe id="scene-view-map-view" data-src="https://richiecarmichael.github.io/sat/index.html"></iframe>

---

<!-- .slide: data-background="../images/bg-5.png" -->

### Landsat viewer

<iframe id="scene-view-map-view" data-src="https://richiecarmichael.github.io/landsat-viewer/index.html"></iframe>
