#include <iostream>
#include<vector>
using namespace std;

void bubbleSort(int arr[], int n){
    for(int i = 0; i<n; i++){
        for(int j=0; j<n-i-1; j++){
            if(arr[j]>arr[j+1]){
                int temp = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = temp;                
            }
        }
    }
}

void printArr(int arr[], int n){
    for(int i=0; i<n; i++){
        cout<<arr[i]<< " ";
    }cout<<endl;
}
int main(){
    int arr[] = {13, 6, 7, 5 ,8, 1, 3, 4};
    int n = sizeof(arr)/sizeof(arr[0]);
    
    return 0;

}
