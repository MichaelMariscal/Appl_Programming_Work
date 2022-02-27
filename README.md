# Appl_Programming_Work

# Overview

The purpose of this software is to be a guide while out on the course for a round of golf! This program is used to track your distance of each hole. It gives some basic information such as the distance from the tee box to the pin, it indicates if it is a par 3-5, along with what hole you are on.

I designed this for a quick and easy guide to help either beginners or professionals out on the course. I also wanted to use this as a guide for anyone who is interested on learning how to golf by just adding the essentials to each hole. For this example, it was set in Pebble Beach out in California.


[Software Demo Video](https://youtu.be/4VS_R8iVugU)

# Development Environment

For this program, I used CodePen. This website was extremely useful as it had tutorials for almost everything related to HTML. I also referenced the ARCGis website as well since it held all of the information for the layering of the maps that are displayed.

# Useful Websites

{Make a list of websites that you found helpful in this project}
* [CodePen](https://codepen.io/following)
* [ARCGis](https://www.arcgis.com/index.html#)

# Future Work

Something that I would like to add in the future would be a GPS tracker. With this, it can track the users location and find the nearest golf club and display information about it.
Another feature I would like to add is a slope indicator. This wouldbe based off of a 3D map and tells the user where the slopes are and what to avoid. For example, green would indicate that the ground is flat. Yellow would be a slight slope and red would be a faster slope if a ball were to land on it.


# Code Source

///
<html>
<head>
<meta charset="utf-8">
<meta name="viewport" content="initial-xscale=1, maximum-scale=1, user-scalable=no">
<title>Golf Distance Program</title>
<style>
  html, body, #viewDiv {
    padding: 0;
    margin: 0;
    height: 100%;
    width: 100%;
  }
</style>

<link rel="stylesheet" href="https://js.arcgis.com/4.22/esri/themes/light/main.css">
<script src="https://js.arcgis.com/4.22/"></script>

<script>
  require([
    "esri/config",
    "esri/Map",
    "esri/views/MapView",
    "esri/Graphic",
    "esri/layers/GraphicsLayer"
  ],(esriConfig, Map, MapView, Graphic, GraphicsLayer)=> {

    esriConfig.apiKey = "AAPKbf097ffaeef94178a980436111d44f96s_1pKskjBL-fnX8d4HZ_uBMNFlJqq01OEgM0VuOnIrqrHoU6oWiV17Besk9PecPX";
    const map = new Map({
      basemap: "arcgis-topographic"
    });
    
    

    const view = new MapView({
      container: "viewDiv",
      map: map,
      center: [-121.9450,36.5687],
      zoom: 15,
      constraints: {
        snapToZoom: false
      }
    });

    const graphicsLayer = new GraphicsLayer();
    map.add(graphicsLayer);

    const point = {
      type: "point",
      longitude: -121.9485,
      latitude: 36.5701
    };
     

    const simpleMarkerSymbol = {
      type: "simple-marker",
      color: [226, 100, 200],
      outline: {
        color: [255, 255, 255],
        width: 1
      }
    };

    const attributes = {
      name: "Point",
      description: "Hole #1 - Distance = 384 - Par 4"
    }
    

    const pointGraphic = new Graphic({
      geometry: point,
      symbol: simpleMarkerSymbol,
      attributes: attributes,
      popupTemplate: {
        title: attributes.name,
        content: attributes.description
      }
    });

    graphicsLayer.add(pointGraphic);
    
       const point2 = {
      type: "point",
      longitude: -121.9460,
      latitude: 36.5702
    };
     

    const simpleMarkerSymbol2 = {
      type: "simple-marker",
      color: [226, 100, 200],
      outline: {
        color: [255, 255, 255],
        width: 1
      }
    };

    const attributes2 = {
      name: "Point",
      description: "Hole #2 - Distance = 518 - Par 5"
    }
    

    const pointGraphic2 = new Graphic({
      geometry: point2,
      symbol: simpleMarkerSymbol2,
      attributes: attributes2,
      popupTemplate: {
        title: attributes2.name,
        content: attributes2.description
      }
    });

    graphicsLayer.add(pointGraphic2);
    
    
    
           const point3 = {
      type: "point",
      longitude: -121.9437,
      latitude: 36.5680
    };
     

    const simpleMarkerSymbol3 = {
      type: "simple-marker",
      color: [226, 100, 200],
      outline: {
        color: [255, 255, 255],
        width: 1
      }
    };

    const attributes3 = {
      name: "Point",
      description: "Hole #3 - Distance = 400 - Par 4"
    }
    

    const pointGraphic3 = new Graphic({
      geometry: point3,
      symbol: simpleMarkerSymbol3,
      attributes: attributes3,
      popupTemplate: {
        title: attributes3.name,
        content: attributes3.description
      }
    });

    graphicsLayer.add(pointGraphic3);
    
    
           const point4 = {
      type: "point",
      longitude: -121.9422,
      latitude: 36.5668
    };
     

    const simpleMarkerSymbol4 = {
      type: "simple-marker",
      color: [226, 100, 200],
      outline: {
        color: [255, 255, 255],
        width: 1
      }
    };

    const attributes4 = {
      name: "Point",
      description: "Hole #4 - Distance = 333 - Par 4"
    }
    

    const pointGraphic4 = new Graphic({
      geometry: point4,
      symbol: simpleMarkerSymbol4,
      attributes: attributes4,
      popupTemplate: {
        title: attributes4.name,
        content: attributes4.description
      }
    });

    graphicsLayer.add(pointGraphic4);
    
        
           const point5 = {
      type: "point",
      longitude: -121.9398,
      latitude: 36.5658
    };
     

    const simpleMarkerSymbol5 = {
      type: "simple-marker",
      color: [226, 100, 200],
      outline: {
        color: [255, 255, 255],
        width: 1
      }
    };

    const attributes5 = {
      name: "Point",
      description: "Hole #5 - Distance = 197 - Par 3"
    }
    

    const pointGraphic5 = new Graphic({
      geometry: point5,
      symbol: simpleMarkerSymbol5,
      attributes: attributes5,
      popupTemplate: {
        title: attributes5.name,
        content: attributes5.description
      }
    });

    graphicsLayer.add(pointGraphic5);
    

    
        
           const point6 = {
      type: "point",
      longitude: -121.9390,
      latitude: 36.5645
    };
     

    const simpleMarkerSymbol6 = {
      type: "simple-marker",
      color: [226, 100, 200],
      outline: {
        color: [255, 255, 255],
        width: 1
      }
    };

    const attributes6 = {
      name: "Point",
      description: "Hole #6 - Distance = 522 - Par 5"
    }
    

    const pointGraphic6 = new Graphic({
      geometry: point6,
      symbol: simpleMarkerSymbol6,
      attributes: attributes6,
      popupTemplate: {
        title: attributes6.name,
        content: attributes6.description
      }
    });

    graphicsLayer.add(pointGraphic6);
    
    
    
               const point7 = {
      type: "point",
      longitude: -121.9400,
      latitude: 36.5617
    };
     

    const simpleMarkerSymbol7 = {
      type: "simple-marker",
      color: [226, 100, 200],
      outline: {
        color: [255, 255, 255],
        width: 1
      }
    };

    const attributes7 = {
      name: "Point",
      description: "Hole #7 - Distance = 111 - Par 3"
    }
    

    const pointGraphic7 = new Graphic({
      geometry: point7,
      symbol: simpleMarkerSymbol7,
      attributes: attributes7,
      popupTemplate: {
        title: attributes7.name,
        content: attributes7.description
      }
    });

    graphicsLayer.add(pointGraphic7);
    
    
    const point8 = {
      type: "point",
      longitude: -121.9385,
      latitude: 36.5625
    };
     

    const simpleMarkerSymbol8 = {
      type: "simple-marker",
      color: [226, 100, 200],
      outline: {
        color: [255, 255, 255],
        width: 1
      }
    };

    const attributes8 = {
      name: "Point",
      description: "Hole #8 - Distance = 424 - Par 4"
    }
    

    const pointGraphic8 = new Graphic({
      geometry: point8,
      symbol: simpleMarkerSymbol8,
      attributes: attributes8,
      popupTemplate: {
        title: attributes8.name,
        content: attributes8.description
      }
    });

    graphicsLayer.add(pointGraphic8);
    
    
    const point9 = {
      type: "point",
      longitude: -121.9345,
      latitude: 36.5617
    };
    

    const simpleMarkerSymbol9 = {
      type: "simple-marker",
      color: [226, 100, 200],
      outline: {
        color: [255, 255, 255],
        width: 1
      }
    };

    const attributes9 = {
      name: "Point",
      description: "Hole #9 - Distance = 526 - Par 4"
    }
    

    const pointGraphic9 = new Graphic({
      geometry: point9,
      symbol: simpleMarkerSymbol9,
      attributes: attributes9,
      popupTemplate: {
        title: attributes9.name,
        content: attributes9.description
      }
    });

    graphicsLayer.add(pointGraphic9);
    
    
     const point10 = {
      type: "point",
      longitude: -121.9319,
      latitude: 36.5598
    };
    

    const simpleMarkerSymbol10 = {
      type: "simple-marker",
      color: [226, 100, 200],
      outline: {
        color: [255, 255, 255],
        width: 1
      }
    };

    const attributes10 = {
      name: "Point",
      description: "Hole #10 - Distance = 495 - Par 4"
    }
    

    const pointGraphic10 = new Graphic({
      geometry: point10,
      symbol: simpleMarkerSymbol10,
      attributes: attributes10,
      popupTemplate: {
        title: attributes10.name,
        content: attributes10.description
      }
    });

    graphicsLayer.add(pointGraphic10);
    
    
     const point11 = {
      type: "point",
      longitude: -121.9303,
      latitude: 36.5595
    };
    

    const simpleMarkerSymbol11 = {
      type: "simple-marker",
      color: [226, 100, 200],
      outline: {
        color: [255, 255, 255],
        width: 1
      }
    };

    const attributes11 = {
      name: "Point",
      description: "Hole #11 - Distance = 388 - Par 4"
    }
    

    const pointGraphic11 = new Graphic({
      geometry: point11,
      symbol: simpleMarkerSymbol11,
      attributes: attributes11,
      popupTemplate: {
        title: attributes11.name,
        content: attributes11.description
      }
    });

    graphicsLayer.add(pointGraphic11);
    
    
    const point12 = {
      type: "point",
      longitude: -121.9313,
      latitude: 36.5613
    };
    

    const simpleMarkerSymbol12 = {
      type: "simple-marker",
      color: [226, 100, 200],
      outline: {
        color: [255, 255, 255],
        width: 1
      }
    };

    const attributes12 = {
      name: "Point",
      description: "Hole #12 - Distance = 212 - Par 3"
    }
    

    const pointGraphic12 = new Graphic({
      geometry: point12,
      symbol: simpleMarkerSymbol12,
      attributes: attributes12,
      popupTemplate: {
        title: attributes12.name,
        content: attributes12.description
      }
    });

    graphicsLayer.add(pointGraphic12);
    
    
    const point13 = {
      type: "point",
      longitude: -121.9345,
      latitude: 36.5629
    };
    

    const simpleMarkerSymbol13 = {
      type: "simple-marker",
      color: [226, 100, 200],
      outline: {
        color: [255, 255, 255],
        width: 1
      }
    };

    const attributes13 = {
      name: "Point",
      description: "Hole #13 - Distance = 447 - Par 4"
    }
    

    const pointGraphic13 = new Graphic({
      geometry: point13,
      symbol: simpleMarkerSymbol13,
      attributes: attributes13,
      popupTemplate: {
        title: attributes13.name,
        content: attributes13.description
      }
    });

    graphicsLayer.add(pointGraphic13);
    
    const point14 = {
      type: "point",
      longitude: -121.9374,
      latitude: 36.5650
    };
    

    const simpleMarkerSymbol14 = {
      type: "simple-marker",
      color: [226, 100, 200],
      outline: {
        color: [255, 255, 255],
        width: 1
      }
    };

    const attributes14 = {
      name: "Point",
      description: "Hole #14 - Distance = 589 - Par 5"
    }
    

    const pointGraphic14 = new Graphic({
      geometry: point14,
      symbol: simpleMarkerSymbol14,
      attributes: attributes14,
      popupTemplate: {
        title: attributes14.name,
        content: attributes14.description
      }
    });

    graphicsLayer.add(pointGraphic14);
    
    const point15 = {
      type: "point",
      longitude: -121.9401,
      latitude: 36.5692
    };
    

    const simpleMarkerSymbol15 = {
      type: "simple-marker",
      color: [226, 100, 200],
      outline: {
        color: [255, 255, 255],
        width: 1
      }
    };

    const attributes15 = {
      name: "Point",
      description: "Hole #15 - Distance = 398 - Par 4"
    }
    

    const pointGraphic15 = new Graphic({
      geometry: point15,
      symbol: simpleMarkerSymbol15,
      attributes: attributes15,
      popupTemplate: {
        title: attributes15.name,
        content: attributes15.description
      }
    });

    graphicsLayer.add(pointGraphic15);
    
    const point16 = {
      type: "point",
      longitude: -121.9415,
      latitude: 36.5687
    };
    

    const simpleMarkerSymbol16 = {
      type: "simple-marker",
      color: [226, 100, 200],
      outline: {
        color: [255, 255, 255],
        width: 1
      }
    };

    const attributes16 = {
      name: "Point",
      description: "Hole #16 - Distance = 403 - Par 4"
    }
    

    const pointGraphic16 = new Graphic({
      geometry: point16,
      symbol: simpleMarkerSymbol16,
      attributes: attributes16,
      popupTemplate: {
        title: attributes16.name,
        content: attributes16.description
      }
    });

    graphicsLayer.add(pointGraphic16);
    
    const point17 = {
      type: "point",
      longitude: -121.9447,
      latitude: 36.5663
    };
    

    const simpleMarkerSymbol17 = {
      type: "simple-marker",
      color: [226, 100, 200],
      outline: {
        color: [255, 255, 255],
        width: 1
      }
    };

    const attributes17 = {
      name: "Point",
      description: "Hole #17 - Distance = 210 - Par 3"
    }
    

    const pointGraphic17 = new Graphic({
      geometry: point17,
      symbol: simpleMarkerSymbol17,
      attributes: attributes17,
      popupTemplate: {
        title: attributes17.name,
        content: attributes17.description
      }
    });

    graphicsLayer.add(pointGraphic17);
    
    const point18 = {
      type: "point",
      longitude: -121.9475,
      latitude: 36.5675
    };
    

    const simpleMarkerSymbol18 = {
      type: "simple-marker",
      color: [226, 100, 200],
      outline: {
        color: [255, 255, 255],
        width: 1
      }
    };

    const attributes18 = {
      name: "Point",
      description: "Hole #18 - Distance = 539 - Par 5"
    }
    

    const pointGraphic18 = new Graphic({
      geometry: point18,
      symbol: simpleMarkerSymbol18,
      attributes: attributes18,
      popupTemplate: {
        title: attributes18.name,
        content: attributes18.description
      }
    });

    graphicsLayer.add(pointGraphic18);
    
    
  });
</script>
</head>
<body>
  <div id="viewDiv"></div>
</body>
</html>
///
