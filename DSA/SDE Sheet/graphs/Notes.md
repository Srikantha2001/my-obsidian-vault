- Graphs G= (V,E)
	- V = set of vertices
	- E = set of Edges
- ![[Pasted image 20241007052200.png]]
	- For the above graph 
		- V={ 1, 2, 3, 4, 5}
		- E= { (1,2),(1,5),(2,1),(2,3),(2,4),(2,5), (3,2),(3,4),(4,2),(4,3),(4,5),(5,1),(5,2),((5,4))}

- Undirected and Directed Graph
- source and sink
- path
- Reachable Node
- Directed Acyclic graph.
- Topological Ordering
- Number of connected Components


## Adjacency List and Adjacency Matrix

```Java
package io.sriki;  
  
import java.util.*;  
  
  
public class Solution {  
  
  
    public List<List<Integer>> getAdjacencyList(int n, int[][] edgeArray) {  
        /*  
                Creating Adjacency List Representation of Graph         */        List<List<Integer>> adjacencyList = new ArrayList<>();  
        for(int i=0;i<n;i++){  
            adjacencyList.add(new ArrayList<>());  
        }  
  
        for(int []edge : edgeArray){  
            adjacencyList.get(edge[0]).add(edge[1]);  
            adjacencyList.get(edge[1]).add(edge[0]);  
        }  
        return adjacencyList;  
    }  
  
    public Boolean[][] getAdjacencyMatrix(int n, int[][] edgeArray) {  
        /*  
                Creating Adjacency Matrix Representation Of Graph         */        Boolean[][] adjMatrix = new Boolean[n][n];  
  
        for(int []edge : edgeArray){  
            adjMatrix[edge[0]][edge[1]] = true;  
            adjMatrix[edge[1]][edge[0]] = true;  
        }  
        return adjMatrix;  
    }  
}
```