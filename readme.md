# knowledge graph experiments
# experiments with knowledge graph stuff

uses py2neo

get neo4j running on your machine; make a new graph, give it a password, start the graph

install py2neo. `pip install --upgrade py2neo` should work; failing that use

```
pip install git+https://github.com/technige/py2neo.git@master#egg=py2neo
```

memo to self: use the 'yates' env. start the neo4j graph database too, first.

also, re neo4j - install apoc for the individual graph. Also, each individual graph has its own conf file. you have to enable export within the particular graph file. go to the graph database settings, open in finder, and use *that* conf. Add things like

'apoc.export.file.enabled=true'

then can export with cypher: `cALL apoc.export.graphml.all("output.graphml", {})`

the resulting file - output.graphml - will be in the `input` folder for your database (path to which you can find by hitting 'open folder' in the graph settings in neo4j)
