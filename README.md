/*sq root using binary search */
#include<bits/stdc++.h>
using namespace std ; 

long long int sqrtInteger(n){
    int s=0;  int e = n;
    long long ans = -1;
    long long mid = s + (e-s)/2;
    while(s<=e)
    {
      long long int square = mid * mid ; 
      if(square == n){
      return mid;
      }
      if(square<n){
      ans = mid;
      s = mid +1;
      }
      else{
      e= mid -1;
      }
      mid = s +(e-s)/2;
     }
     return ans;
 }
 
 
 int main(){
 int n;cin>>n;
 cout<<"only int part is " << sqrtInteger(n)<<endl;
 return 0;
 }
  
