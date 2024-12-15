---
layout: post
title: Flake it till you make it
subtitle: Excerpt from Soulshaping by Jeff Brown
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
tags: [books, test]
author: Sharon Smith and Barry Simpson
---

<html>
<head>
  <style>
    .chart-container {
      display: none;
    }
    .chart-container.active {
      display: block;
    }
    .button-group button {
      margin: 5px;
      padding: 10px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <!-- 按钮组 -->
  <div class="button-group">
    <button onclick="showChart('chart1')">图表 1</button>
    <button onclick="showChart('chart2')">图表 2</button>
    <button onclick="showChart('chart3')">图表 3</button>
  </div>
  
  <!-- 图表容器 -->
  <div id="chart1" class="chart-container active">
    <div class="flourish-embed flourish-chart" data-src="visualisation/20802185">
      <script src="https://public.flourish.studio/resources/embed.js"></script>
      <noscript>
        <img src="https://public.flourish.studio/visualisation/20802185/thumbnail" width="100%" alt="chart visualization" />
      </noscript>
    </div>
  </div>

  <div id="chart2" class="chart-container active">
    <div class="flourish-embed flourish-chart" data-src="visualisation/20802185">
      <script src="https://public.flourish.studio/resources/embed.js"></script>
      <noscript>
        <img src="https://public.flourish.studio/visualisation/20802185/thumbnail" width="100%" alt="chart visualization" />
      </noscript>
    </div>
  </div>

  <div id="chart3" class="chart-container active">
    <div class="flourish-embed flourish-chart" data-src="visualisation/20802185">
      <script src="https://public.flourish.studio/resources/embed.js"></script>
      <noscript>
        <img src="https://public.flourish.studio/visualisation/20802185/thumbnail" width="100%" alt="chart visualization" />
      </noscript>
    </div>
  </div>

  <script>
    // JavaScript 函数用于切换图表
    function showChart(chartId) {
      const charts = document.querySelectorAll('.chart-container');
      charts.forEach(chart => {
        chart.classList.remove('active');
      });
      document.getElementById(chartId).classList.add('active');
    }
  </script>
</body>
</html>
