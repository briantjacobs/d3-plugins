# Sankey Diagrams

Demo: <http://bl.ocks.org/briantjacobs/9608831/>  
Demo gist: <https://gist.github.com/briantjacobs/9608831>  
Blog post: <http://briantjacobs.com/d3-sankey-schema>

Sankey plugin with optional schema function.
Plugin now accepts arbitary field names and allows making reference to IDs within nodes rather than index-based nodes.
Plugin now accepts floatRight option (default true) that makes pushing terminal nodes to the right optional.

```js
var sankey = d3.sankey()
    .size([width, height])
    .floatRight(false) // defaultTrue
    .nodeWidth(15)
    .nodePadding(10)
    .nodes(energy.nodes)
    .links(energy.links)
    .layout(32)
	.schema({
	          id: "id",
	          source: "fuel_origin",
	          target: "fuel_desc",
	          value: "val"
	      });
    ;
```

```
var path = sankey.link();
```
