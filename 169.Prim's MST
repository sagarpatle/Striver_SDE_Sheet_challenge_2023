#include <bits/stdc++.h> 
vector<pair<pair<int, int>, int>> calculatePrimsMST(int n, int m, vector<pair<pair<int, int>, int>> &g)
{
    // Prim's Algorithm
    // Time Complexity: O(n^2)
    // Space Complexity: O(n + m)
    // Adjacency List
    vector<vector<pair<int, int>>> adj(n + 1);
    for(auto edge : g){
        adj[edge.first.first].push_back(make_pair(edge.first.second, edge.second));
        adj[edge.first.second].push_back(make_pair(edge.first.first, edge.second));
    }
    // Key Array
    vector<int> key(n + 1, INT_MAX);
    // MST Array
    vector<bool> mst(n + 1, false);
    // Parent Array
    vector<int> parent(n + 1, -1);
    // Prim's Algorithm
    // assume 1 as the root node
    key[1] = 0;
    for(int i = 0; i < n; i++){
        // Step 1: find the minimum key which is not in the mst.
        int mini = INT_MAX;
        int u = -1;
        for(int i = 1; i <= n; i++){
            if(key[i] < mini && !mst[i]){
                mini = key[i];
                u = i;
            }
        }
        // Step 2: mark the minimum node as mst visited
        mst[u] = true;
        // Step 3: travel all it's neighbours and update there keys
        for(auto neighbour : adj[u]){
            if(!mst[neighbour.first] && key[neighbour.first] > neighbour.second){
                key[neighbour.first] = neighbour.second;
                parent[neighbour.first] = u;
            }
        } 
    }
    vector<pair<pair<int,int>,int>> ans;
    for(int i = 2; i <= n; i++){
        ans.push_back(make_pair(make_pair(i, parent[i]),key[i]));
        // ans.push_back(make_pair(make_pair(parent[i], i),key[i]));
    }
    return ans;
}
