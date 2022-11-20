---
author: Hugo Authors
title: Math Typesetting
date: 2019-03-08
description: A brief guide to setup KaTeX
math: true
toc: true
tags:
 - math
categories:
    - data-science
---

## Welcome to the world of proper typesetting

Mathematical notation in a Hugo project can be enabled by using third party JavaScript libraries.
<!--more-->

In this example we will be using [KaTeX](https://katex.org/)

- Create a partial under `/layouts/partials/math.html`
- Within this partial reference the [Auto-render Extension](https://katex.org/docs/autorender.html) or host these scripts locally.
- Include the partial in your templates like so:  

```bash
{{ if or .Params.math .Site.Params.math }}
{{ partial "math.html" . }}
{{ end }}
```

- To enable KaTex globally set the parameter `math` to `true` in a project's configuration
- To enable KaTex on a per page basis include the parameter `math: true` in content files

**Note:** Use the online reference of [Supported TeX Functions](https://katex.org/docs/supported.html)

{{< math.inline >}}
{{ if or .Page.Params.math .Site.Params.math }}
<!-- KaTeX -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/katex.min.css" integrity="sha384-zB1R0rpPzHqg7Kpt0Aljp8JPLqbXI3bhnPWROx27a9N0Ll6ZP/+DiW/UqRcLbRjq" crossorigin="anonymous">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/katex.min.js" integrity="sha384-y23I5Q6l+B6vatafAwxRu/0oK/79VlbSz7Q9aiSZUvyWYIYsd+qj+o24G5ZU2zJz" crossorigin="anonymous"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/contrib/auto-render.min.js" integrity="sha384-kWPLUVMOks5AQFrykwIup5lo0m3iMkkHrD0uJ4H5cjeGihAutqP0yW0J6dpFiVkI" crossorigin="anonymous" onload="renderMathInElement(document.body);"></script>
{{ end }}
{{</ math.inline >}}

### Examples

{{< math.inline >}}
<p>
Inline math: \(\varphi = \dfrac{1+\sqrt5}{2}= 1.6180339887…\)
</p>
{{</ math.inline >}}

Block math:
$$
 \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } } 
$$


Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus fringilla nibh orci, ac tincidunt felis congue a. Ut vehicula euismod lectus nec pellentesque. Sed at eleifend velit. Donec quis elementum est. Aliquam vulputate dolor vitae lectus hendrerit, sed finibus urna blandit. Maecenas sit amet lobortis dui. Sed molestie consequat nulla, sed feugiat dui venenatis vel. Nam commodo erat scelerisque elementum elementum. Curabitur aliquam ex et nibh molestie, ut lacinia ipsum rutrum. Aliquam in augue neque. Integer interdum magna quis lectus gravida efficitur. Curabitur quis velit erat. Cras ut magna vitae urna finibus cursus. Vivamus dictum turpis at ante faucibus, non tristique massa fermentum. Curabitur vestibulum nunc id varius placerat. Aenean ligula nisi, placerat in congue nec, faucibus non nibh.

## Test

Nulla fringilla vitae eros ac vestibulum. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut vitae dignissim urna. Nam rhoncus, enim quis lacinia rhoncus, leo ante blandit lacus, vel sagittis massa mi nec libero. Etiam posuere neque vitae cursus finibus. Nunc sed enim a ligula convallis venenatis laoreet eget purus. Ut varius eget diam ut accumsan.

Quisque a ex velit. Mauris sodales ex ut consectetur semper. Vestibulum volutpat velit non augue mollis, eu consectetur sapien aliquet. Duis suscipit ipsum venenatis magna suscipit fermentum. Suspendisse at nulla feugiat, lobortis lacus sed, rhoncus elit. Quisque non tempor metus. Quisque et viverra risus. Ut volutpat erat vitae purus dignissim, in blandit justo posuere. Etiam in magna nunc. Aliquam sed aliquet mi, non laoreet lectus. Nullam vel sem tellus. Proin varius est velit, non tempus nisi facilisis at. Suspendisse pellentesque placerat nulla id suscipit. Maecenas ut mauris eget nulla faucibus dapibus ac sed dui.

Etiam consequat ut magna et varius. Mauris sit amet sem finibus neque elementum fermentum. Donec at tincidunt turpis. Quisque tristique dapibus urna vitae semper. Praesent sit amet elit nec massa viverra venenatis eu eu risus. Suspendisse aliquet lacus et elit ullamcorper venenatis. Suspendisse fermentum est diam, id imperdiet orci tristique fermentum. Aenean non sem scelerisque, viverra enim id, viverra ipsum. Nullam non congue quam, sed malesuada justo.

Praesent eget efficitur magna. Suspendisse cursus non quam id accumsan. Curabitur ut sodales tortor. Praesent scelerisque porta sapien, vitae tempor sapien porttitor ac. Sed dictum luctus sollicitudin. Aenean a pharetra mi, ut pharetra ex. Maecenas mauris turpis, lobortis nec tempor a, efficitur vel eros. Sed posuere vitae enim eu vehicula. Pellentesque vestibulum dui sit amet nibh porttitor dignissim. Quisque porta mattis odio, id venenatis mauris ultricies eu. Nulla sit amet ultricies nibh. Fusce rhoncus viverra lacus sit amet aliquet. Nam porta a sapien in aliquam. In et metus id arcu blandit volutpat. Pellentesque at erat elit.