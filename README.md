# DSA
Second Smallest and Second Largest without Sorting
#include <bits/stdc++.h>
using namespace std;

void secLarSmall(int arr[], int n){
    if(n==0 || n==1)
    cout<<"Small = -1" <<"   "<<"Large = -1"<<endl;
    int small = INT_MAX ,secondsmall = INT_MAX;
    int large = INT_MIN ,secondlarge = INT_MIN;
    for(int i=0; i<n;i++){
        small = min(small,arr[i]);
        large = max(large,arr[i]);
    }
    cout<<"Small: "<<small<<"     "<<"Large: "<<large<<endl;
    
    for(int i=0; i<n; i++){
        if(secondsmall > arr[i] && arr[i] != small)
            secondsmall = arr[i];
        if(secondlarge < arr[i] && arr[i] != large)
            secondlarge = arr[i];
    }
    cout<<"Second smallest : "<<secondsmall<<"      "<<"Second largest : "<<secondlarge<<endl;
}

int main(){
    int arr[] = {1,8,3,9,5,2,6};
    int n = sizeof(arr)/sizeof(arr[0]);
    secLarSmall(arr,n);
    
}
