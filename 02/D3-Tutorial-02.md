# D3 Tutorial
[The Advanced Web Developer Bootcamp](https://www.udemy.com/the-advanced-web-developer-bootcamp/)

## Event Listeners


## 223 Event Listeners in D3

### Add listener with the *on* method.

```
d3.select("h1").on("click", () => {  
  console.log("Listening for clicks on h1!");
  });
```

### Remove listener with *null* as second argument to the *on* method.

```
d3.select("h1").on("click", null);
```

### Access events with the *d3.event* property.

```
d3.select("#new-note").on("submit", () => {
  d3.event.preventDefault();

  var input = d3.select("input");
  d3.select("#notes")
    .append("p")
      .classed("note", true)
      .text(input.property("value"));  
    // clear the form  
    input.property("value", "");
  });
```



## Remove DOM elements with *remove*.

```
d3.selectAll("p").remove();
```
