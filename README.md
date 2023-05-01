# food-network
Neo4j network of information about recipes and ingredients (h/t Rik Van Bruggen and Yong-Yeol Ahn)

# Credit
This graph database is based on the work of 
[Rik Van Bruggen](https://blog.bruggen.com/2013/12/fascinating-food-networks-in-neo4j.html) 
and
[Yong-Yeol Ahn](http://www.yongyeol.com).

# Requirements
- Neo4j 5.5 or 5.7
- APOC 5.7
- Bash
- Cypher shell

# Installation steps - local Neo4j installation

- Install Neo4j Enterprise Edition version 5.7
- In `neo4j.conf`, set `dbms.memory.transaction.total.max=1024m`.
- Start the Neo4j server and set up an empty database with username password `food-network`
- Install the APOC plug-in version 5.7
- Install Neo4j shell and make sure that `cypher-shell` is in your bash path
- In bash: `./run-make-food-database.sh`


# Installation steps - Neo4j sandbox

- In the Neo4j sandbox browser, run this Cypher command:

```
call apoc.cypher.runFile('https://raw.githubusercontent.com/ramseylab/food-network/main/make-food-database.cql');
```

which runs the script [`make-food-database.cql` (github)](https://github.com/ramseylab/food-network/blob/main/make-food-database.cql).
