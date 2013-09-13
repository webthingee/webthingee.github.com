---
layout: post
image: /img/jekyll.png
title:  "Snippet - Jekyll"
date:   2013-07-31 06:59:02
categories: code snippet jekyll
---

In order to use angularjs with jekyll, I needed to find a way to excape curly brackets so they would be available to the DOM.  The result was...

  <div class="panel">
    ![jekyllexcape](/img/excapejekyll.png)
  </div>

  <div class="panel callout">
    <label>Name:</label>
    <input type="text" ng-model="yourName1" placeholder="Enter a name here">
    <hr>
    <h1>Hello {{"{{ yourName1"}}}}!</h1>
  </div>

Or if I placed the markup I needed into a file, and placed it into a views directory, I was able to call it with...

  <div class="panel">
      ```<div ng-include="'/views/nav.html'"></div>
      ```
  </div>

  <div class="panel callout">
    <div ng-include="'/views/nav.html'"></div>
  </div>
