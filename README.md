# Pubg



#include<bits/stdc++.h>
#define v(x) vector<x>
#define pb(x) push_back(x)
#define fori0(i,n)
  for(int i=0;i<n;i++)
#define in(n) int n;cin>>n
using namespace std;
const int MAX=1e5+2;
v(int) tree[MAX];
bool vis[MAX];
int start,curlength=0;
void dfs(int s,int len){
vis[s]=true;
if(len>curlength) {start=s;curlength=len;}
for(auto i:tree[s])
  vis[s]=true;
if(len>curlength) {start=s;curlength=len;}
for(auto i:tree[s])
if(!vis[i])
dfs(i,len+1);
}
int main()
{
ios_base::sync_with_stdio(false);cin.tie(NULL);
in(n);
fori0(i,n){
in(x);in(y);
tree[x].pb(y);tree[y].pb(x);
}
dfs(1,1);
cout<<start<<" ";
memset(vis,false,n);
curlength=0;
dfs(start,1);
cout<<start;
return 0;
}

  







  
  
