/*
author laxman Sharma
input format:
V : no. of vertices
e: no. edges
then next e lines contains 3 integer 
u v, w : there is directed edge between u to v with weight w
s: source from where we need to calculate the distance of others
*/
#include<bits/stdc++.h>
using namespace std;
int main() {
	int V;
	cin>>V;
	int e;
	cin>>e;
	vector<vector<int>> edges;
	for(int i=0;i<e;i++) {
		int u,v,w;
		cin>>u>>v>>w;
		edges.push_back({u,v,w});
	}
	int s;
	cin>>s;
	vector<int> dist(V, INT_MAX);
	dist[s] = 0;

	for(int i=0;i<V;i++) {
		for(int j=0;j<e;j++) {
			int u = edges[j][0];
			int v = edges[j][1];
			int w = edges[j][2];
			if(dist[u] + w < dist[v] && dist[u] != INT_MAX) {
				dist[v] = dist[u] + w;
			}
		}
	}

	cout<<"distance from source node: "<<s<<"to all other nodes is: "<<endl;
	for(int i=0;i<V;i++) {
		cout<<"distance of Node: "<<i<<"from source is : "<<dist[i]<<endl;
	}
}
