---
title: Code Syntax
date: 2012-09-11
tags: markdown, syntax
---

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
