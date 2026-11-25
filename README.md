{
  "name": "Markel Claims Theme",
  "dataColors": [
    "#FF4E00",
    "#246C7B",
    "#424242",
    "#BAB79D",
    "#A39990",
    "#D32300",
    "#DBD6D3",
    "#F4F2EB"
  ],
  "background": "#FFFFFF",
  "secondaryBackground": "#DBD6D3",
  "foreground": "#424242",
  "foregroundNeutralSecondary": "#A39990",
  "foregroundNeutralTertiary": "#DBD6D3",
  "backgroundLight": "#F4F2EB",
  "backgroundNeutral": "#DBD6D3",
  "tableAccent": "#FF4E00",
  "good": "#246C7B",
  "neutral": "#BAB79D",
  "bad": "#D32300",
  "maximum": "#246C7B",
  "center": "#F4F2EB",
  "minimum": "#FF4E00",
  "textClasses": {
    "title": { "fontFace": "Segoe UI Semibold", "fontSize": 14, "color": "#424242" },
    "header": { "fontFace": "Segoe UI Semibold", "fontSize": 12, "color": "#424242" },
    "label": { "fontFace": "Segoe UI", "fontSize": 10, "color": "#424242" },
    "callout": { "fontFace": "Segoe UI Semibold", "fontSize": 28, "color": "#424242" }
  },
  "visualStyles": {
    "page": {
      "*": {
        "background": [{ "color": { "solid": { "color": "#F4F2EB" } }, "transparency": 0 }],
        "outspace": [{ "color": { "solid": { "color": "#F4F2EB" } }, "transparency": 0 }]
      }
    },
    "*": {
      "*": {
        "background": [{ "show": true, "color": { "solid": { "color": "#FFFFFF" } }, "transparency": 0 }],
        "border": [{ "show": true, "color": { "solid": { "color": "#DBD6D3" } }, "radius": 10 }],
        "title": [{ "fontColor": { "solid": { "color": "#424242" } } }]
      }
    },
    "tableEx": {
      "*": {
        "columnHeaders": [{
          "fontColor": { "solid": { "color": "#FFFFFF" } },
          "backColor": { "solid": { "color": "#424242" } }
        }],
        "values": [{
          "fontColorPrimary": { "solid": { "color": "#424242" } },
          "backColorPrimary": { "solid": { "color": "#FFFFFF" } },
          "fontColorSecondary": { "solid": { "color": "#424242" } },
          "backColorSecondary": { "solid": { "color": "#F4F2EB" } }
        }],
        "grid": [{ "gridHorizontalColor": { "solid": { "color": "#DBD6D3" } } }]
      }
    },
    "pivotTable": {
      "*": {
        "columnHeaders": [{
          "fontColor": { "solid": { "color": "#FFFFFF" } },
          "backColor": { "solid": { "color": "#424242" } }
        }],
        "rowHeaders": [{ "fontColor": { "solid": { "color": "#424242" } } }],
        "values": [{
          "backColorPrimary": { "solid": { "color": "#FFFFFF" } },
          "backColorSecondary": { "solid": { "color": "#F4F2EB" } }
        }]
      }
    },
    "slicer": {
      "*": {
        "header": [{ "fontColor": { "solid": { "color": "#424242" } } }],
        "items": [{
          "fontColor": { "solid": { "color": "#424242" } },
          "background": { "solid": { "color": "#FFFFFF" } }
        }]
      }
    },
    "card": {
      "*": {
        "labels": [{ "color": { "solid": { "color": "#FF4E00" } } }],
        "categoryLabels": [{ "color": { "solid": { "color": "#424242" } } }]
      }
    },
    "textbox": {
      "*": {
        "background": [{ "show": false }],
        "border": [{ "show": false }]
      }
    }
  }
}

