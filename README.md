# Codeforcescpp-337A
#include <bits/stdc++.h>

using namespace std;

int main(){
  int n,m,ele;
  vector<int> f;

  cin >> n >> m;

  for(int i=0;i<m;i++){
    cin >> ele;
    f.push_back(ele);
  }
  int diff;
  sort(f.begin(),f.end());
  int min = f.at(n-1) - f.at(0);
  for(int i=1;i<m-n+1;i++){
    diff = f.at(i+n-1) - f.at(i);
    if(min > diff){
      min = diff;
    }
  } 
  cout << min;
  return 0;
}
