---
title: LaTeX
subtitle: A Perfect way to be Perfect
author: David Raj Micheal
job: Reseach Scholar, Department of Statistics 
# logo: slidify_logo.png
# biglogo: slidify_logo.png
# license: by-nc-sa
widgets: [mathjax, bootstrap, quiz]
# github: {user: ramnathv, repo: slidify}
# download: 'io2012.zip'
url: {lib: ../../libraries}
mode: selfcontained
hitheme: tomorrow
assets: {js: 'test.js'}
--- dt:10



## How many of you got the following experiances? ##

<style> 
body { 
  background-color: #111; 
} 
.quiz-option label{ 
  display: inline; 
  font-size: 1em; 
} 
ul.nav li::before { content: ""; }   
ul.nav li{ font-size: 18px; line-height: 24px;} 
</style> 

 <img src="figure/microsoft-word-has-stopped-working.jpg" width = "500px">
 <img src ="figure/MS Word Error.png" width = "500px">

--- .YAML &masthead
## How many of you got the following experiances? ##

<img src = "figure/office-repair-ready.png" width = "500px">
<img src = "figure/word2013_error1.png" width = "500px">

---

## How often you think of these questions? ##



"The file cannot be opened"

--- {class: class, tpl: tabs}

This is to test if the tab template works correctly

*** {class: active, id: problem}

Tab1
fgf
fggh

*** {id: questions}

Tab2

*** {id: variables}

Tab3

---
  
Setext Header
---
  
  
This slide shows a Setext style header.

--- 
  
## Tables
  
Mardown tables contain `---` and should not be interpreted as separator.

Column X | Column Y
---------|----------
Row 1    | Row 1
Row 2    | Row 2


--- bg:#662c91
  
## Animated List, Ordered
  
This list should be animated

> 1. Point 1
> 2. Point 2
> 3. Point 3

---
  
## Animated List, Unordered
  
This list should be animated

> - Point 1
> - Point 2
> - Point 3


---

## Mathjax ##

$$
\begin{aligned}
\nabla \times \vec{\mathbf{B}} -\, \frac1c\, \frac{\partial\vec{\mathbf{E}}}{\partial t} & = \frac{4\pi}{c}\vec{\mathbf{j}} \\   \nabla \cdot \vec{\mathbf{E}} & = 4 \pi \rho \\
\nabla \times \vec{\mathbf{E}}\, +\, \frac1c\, \frac{\partial\vec{\mathbf{B}}}{\partial t} & = \vec{\mathbf{0}} \\
\nabla \cdot \vec{\mathbf{B}} & = 0 \end{aligned}
$$
<br />
$$
\mathbf{V}_1 \times \mathbf{V}_2 =  \begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial X}{\partial u} &  \frac{\partial Y}{\partial u} & 0 \\
\frac{\partial X}{\partial v} &  \frac{\partial Y}{\partial v} & 0
\end{vmatrix}
$$
  
<div class='source'>
  Source: <a href='http://www.subtlepatterns.com'>Background from SubtlePatterns</a>
</div>

--- &twocol

## Layouts, Custom Metadata ##

This is a slide with a two column layout.

*** =left

Column 1

*** =right

Column 2


--- bg:#EEE
  
## Background Color ##
  
This slide should have a subtle gray background.

---

## Background Image ##

This slide should have a background image.

--- &radio

## Widgets: jQuery-Quiz ##

This is a multiple choice question

1. Choice 1
2. `Choice 2`
3. _Choice 3 (correct)_
4. Choice 4

*** .hint

This is a hint

*** .explanation

This is the explanation

---
  
## Widgets: Bootstrap ##
  
**Blocks**
  
<div class="alert alert-info">
 <p>This is an alert info block which should render in blue</p>
</div>
  
**Tooltips**
  
This is to check out tooltips in bootstrap <a href="#" rel="tooltip" data-original-title="Default tooltip">you probably</a>
  
**Popover**
  
<a class="btn btn-large btn-danger" rel="popover" data-content="And here's some amazing content. It's very engaging. right?" data-original-title="A Title" id='example'>Click to toggle popover</a>

<a id='example' data-content='Change directory doesn't actually change the directory. It changes the shell's idea of which directory we are in' data-original-title='Note'><pre>cd data</pre></a>

*** =pnotes

The font size and color needs some tweaking.

---
  
## Highlighter: Highlight JS ##
  
We can make this function more robust by adding a simple error checking statement to prevent illegal parameters from generating invalid results.


```r
qpareto <- function(p, scale, loc) {
  if (( scale <= 0) | ( loc <= 0)) {
    stop("'qpareto' parameters must be greater than zero.")
  }
  q <- loc*(1 - p)^(-1/scale)
  return(q)
}
```

Entering a negative parameter now raises an exception, instead of an invalid result that could silently corrupt subsequent results.


```r
qpareto(0.4, 5, -1)
```

```
## Error in qpareto(0.4, 5, -1): 'qpareto' parameters must be greater than zero.
```
We could improve this further by checking to ensure that `p` is a valid probability.

---
  
## Check Chunk Execution ##
  

```r
library(ggplot2); 
library(ggthemes);
```

```
## Error in library(ggthemes): there is no package called 'ggthemes'
```

```r
qplot(wt, mpg, data = mtcars) +
  theme_solarized()
```

```
## Error in theme_solarized(): could not find function "theme_solarized"
```

*** =pnotes


```r
library(ggplot2); 
library(ggthemes);
qplot(wt, mpg, data = mtcars) +
  theme_solarized()
```

---
  
<q class='shout'>This is a shout</q>
  
I am checking key, <span class = 'key'>key</span>

--- #myslide

<script>
$('#myslide').on('slideenter', function(){
  $(this).find('article')
    .append('<iframe src="http://bl.ocks.org/mbostock/raw/1256572/"></iframe>')
});
$('#myslide').on('slideleave', function(){
  $(this).find('iframe').remove();
});
</script>
