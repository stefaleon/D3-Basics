# D3 Tutorial
[The Advanced Web Developer Bootcamp](https://www.udemy.com/the-advanced-web-developer-bootcamp/)

## DOM Manipulation with D3 methods


## 220 An Introduction to D3

```
d3
{event: null, format: ƒ, formatPrefix: ƒ, timeFormat: ƒ, timeParse: ƒ, …}
```
```
d3.version
"4.13.0"
```


## 221 D3 Selections


```
d3.select("#page-title");
```
```
d3.selectAll("li");
```     

### Accessing Nodes

```
d3.selectAll("li").nodes();
```
```
d3.selectAll("li").node();
```

### Manipulating Selections

```
d3.select("#page-title")
  .style("background-color", "#000000")
  .style("color", "#ffffff")
  .attr("class", "my-class")
  .text("D3 is cool!");
```

### Get properties' values

```
d3.select("#page-title").text();
"D3 is cool!"
```
```
d3.select("li").style("color");
"rgb(0, 0, 0)"
```

### Set classes with *classed* (alternative to *attr*)

```
d3.select("#page-title")
  .classed("my-new-class", true)
```

## 222 Selections and Callbacks

```
d3.selectAll("li")
  .style("font-size", () => {
     return Math.random()*40 + "px";
  });
```

```
d3.selectAll("li")
  .style("background-color", (_, idx) => {
     return idx % 2 === 0 ? "lightgrey" : "white";
  });
```

### Consequent selections with method chaining

```
d3.select(".outer")
    .style("color", "purple")
  .select("div")
    .style("font-size", "30px")
    .style("background-color", "yellow")
  .select("div")
    .style("border", "5px solid green")
```
