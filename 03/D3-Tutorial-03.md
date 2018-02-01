# D3 Tutorial
[The Advanced Web Developer Bootcamp](https://www.udemy.com/the-advanced-web-developer-bootcamp/)

## Data Joins


## 229 Basic Data Joins and Enter Selections

###
```
d3.select("#quotes")
  .style("list-style", "none")
  .selectAll("li")
  .data(quotes)
  .enter()
  .append("li")
    .text( d =>
      '"' + d.quote + '" - ' + d.movie
      + ' (' + d.year + ')' )
      .style("margin", "20px")
      .style("padding", "20px")
      .style("font-size", d =>
        d.quote.length < 25 ? "2em" : "1em")
      .style("background-color", d => colors[d.rating])
      .style("border-radius", "8px");
```
