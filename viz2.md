---
layout: viz
title: test2
nav-menu: true
show_tile: true
---

### Hello
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

<div id="vis2"></div>
<script>
  var vlSpec = {
          "$schema": "https://vega.github.io/schema/vega-lite/v4.json",
          "description": "Textual works by creator excluding unknowns",
          "data": {
      "url": "https://raw.githubusercontent.com/readchina/ReadingData/docker-db/csv/views/view01a_txt-titles.csv"},
          "mark": {
            "type": "bar",
            "tooltip": {
              "content": "data"
            }
          },
          "encoding": {
            "x": {
              "field": "title",
              "type": "ordinal",
              "axis": {
                "labelAngle": 0
              },
              "sort": "-y"
            },
            "y": {
              "aggregate": "count",
              "field": "act_object",
              "type": "quantitative"
            }
          }
        };

  vegaEmbed('#vis2', vlSpec);
</script>
