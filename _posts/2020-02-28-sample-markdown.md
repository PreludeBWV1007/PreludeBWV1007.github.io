---
layout: post
title: Sample blog post to learn markdown tips
subtitle: There's lots to learn!
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [test]
comments: true
mathjax: true
author: Bill Smith
---

{: .box-success}
This is a demo post to show you how to write blog posts with markdown.  I strongly encourage you to [take 5 minutes to learn how to write in markdown](https://markdowntutorial.com/) - it'll teach you how to transform regular text into bold/italics/tables/etc.<br/>I also encourage you to look at the [code that created this post](https://raw.githubusercontent.com/daattali/beautiful-jekyll/master/_posts/2020-02-28-sample-markdown.md) to learn some more advanced tips about using markdown in Beautiful Jekyll.

**Here is some bold text**

## Here is a secondary heading

[This is a link to a different site](https://deanattali.com/) and [this is a link to a section inside this page](#local-urls).

Here's a table:

| Number | Next number | Previous number |
| :------ |:--- | :--- |
| Five | Six | Four |
| Ten | Eleven | Nine |
| Seven | Eight | Six |
| Two | Three | One |

You can use [MathJax](https://www.mathjax.org/) to write LaTeX expressions. For example:
When \\(a \ne 0\\), there are two solutions to \\(ax^2 + bx + c = 0\\) and they are $$x = {-b \pm \sqrt{b^2-4ac} \over 2a}.$$

<!DOCTYPE html>
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


How about a yummy crepe?


![Crepe](https://beautifuljekyll.com/assets/img/crepe.jpg)

It can also be centered!

![Crepe](https://beautifuljekyll.com/assets/img/crepe.jpg){: .mx-auto.d-block :}

Here's a code chunk:

~~~
var foo = function(x) {
  return(x + 5);
}
foo(3)
~~~

And here is the same code with syntax highlighting:

```javascript
var foo = function(x) {
  return(x + 5);
}
foo(3)
```

And here is the same code yet again but with line numbers:

{% highlight javascript linenos %}
var foo = function(x) {
  return(x + 5);
}
foo(3)
{% endhighlight %}

## Boxes
You can add notification, warning and error boxes like this:

### Notification

{: .box-note}
**Note:** This is a notification box.

### Warning

{: .box-warning}
**Warning:** This is a warning box.

### Error

{: .box-error}
**Error:** This is an error box.

## Local URLs in project sites {#local-urls}

When hosting a *project site* on GitHub Pages (for example, `https://USERNAME.github.io/MyProject`), URLs that begin with `/` and refer to local files may not work correctly due to how the root URL (`/`) is interpreted by GitHub Pages. You can read more about it [in the FAQ](https://beautifuljekyll.com/faq/#links-in-project-page). To demonstrate the issue, the following local image will be broken **if your site is a project site:**

![Crepe](/assets/img/crepe.jpg)

If the above image is broken, then you'll need to follow the instructions [in the FAQ](https://beautifuljekyll.com/faq/#links-in-project-page). Here is proof that it can be fixed:

![Crepe]({{ '/assets/img/crepe.jpg' | relative_url }})
