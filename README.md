# Binary-Search
Find an element in sorted array in O(logn) time with binary search method
//Searching in sorted array
#include<iostream>
using namespace std;

int main(){
	int n;
	cin>>n;
	int arr[n];
	for(int i=0;i<n;i++){
		cin>>arr[i];
	}
	int x;
	cout<<"Enter element to be searched: ";
	cin>>x;
	int low=0;
	int high=n-1;
	int cnt=0;
	while(low<=high){
		int mid=(low+high)/2;
		if(arr[mid]=x){
			cnt=mid;
			break;
		}
		else if(arr[mid]>x){
			high=mid-1;
		}
		else{
			low=mid+1;
		}
	}
	if(cnt==0){
		cout<<"Not found";
	}
	else{
		cout<<"Element found at "<<cnt<< " index";
	}
}
