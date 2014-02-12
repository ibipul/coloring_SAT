Author:

 - Bipul Islam
 
---
##K-Coloring with SAT 

Given a Graph( **G** ) and a number of colours ( **K** ), the program says whether the Graph is K colourable. A python script is used to convert the graph to it's SAT in **CNF** form, which is then fed to a SAT solver [**zchaff**](https://www.princeton.edu/~chaff/zchaff.html) which states whether the it's colorable or not or simply undecidable.

####Graph to CNF Mapping
 - For each vertex i in  vertex set V & color c in {1,2... k} use U Xic {c= 1,2...k}.
 - For each i in V, ∩ ∩ (Xic Implies not Xid) where c={1...k-1} & d={c+1...k}.
 - For each edge e(i,j) in G, ∩ (Xic Implies not Xjc) c={1,2...k}.

####Usage:
```
./graph2cnf.py graph_i.txt > graph_i.cnf
./zchaff graph_i.cnf
```
##### Zchaff 
*source (ver--2008.10.12) is included in the project rep as a* **.zip**, *extract and then use* **make** *(Makefile is included in the source) to create the executable it then copy the executable to any location and run as mentioned before*

   
