---
title: Code Syntax
date: 2012-09-11
tags: markdown, syntax
---

Example of YAML markup:

``` yaml
friends:
  - Tom
  - Dick
  - Harry
```

Now, anywhere in our template files, we will have access to this data:

``` html
<h1>Friends</h1>
<ol>
  <% data.people.friends.each do |f| %>
  <li><%= f %></li>
  <% end %>
</ol>
```

Which will render:

``` html
<h1>Friends</h1>
<ol>
  <li>Tom</li>
  <li>Dick</li>
  <li>Harry</li>
</ol>
```

``` coffeescript
#= require "jquery"

$(document).ready ->
  $(".item").pluginCode
    param1: true
    param2: "maybe"
```

The output of this file will be the jQuery library at the code and then the app code, compiled into Javascript, beneath.

You could also write your app file in regular Javascript with a file named `app.js` which looks like this:

``` javascript
//= require "jquery"

$(document).ready(function() {
  $(".item").pluginCode({
    param1: true,
    param2: "maybe"
  });
});
```
