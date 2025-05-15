#include <iostream>
using namespace std;

int partition(int arr[], int st, int end) {
    int pivot = arr[end];  
    int i = st - 1;        

    for (int j = st; j < end; j++) {
        if (arr[j] < pivot) {
            i++;
            swap(arr[i], arr[j]);
        }
    }
    swap(arr[i + 1], arr[end]);  
    return i + 1;              
}

void quickSort(int arr[], int st, int end) {
    if (st < end) {
        int pivIdx = partition(arr, st, end);
        quickSort(arr, st, pivIdx - 1);
        quickSort(arr, pivIdx + 1, end);
    }
}

void printArr(int arr[], int n) {
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
}

int main() {
    int arr[] = {13, 6, 7, 5, 8, 1, 3, 4};
    int n = sizeof(arr) / sizeof(arr[0]);

    cout << "Original array: ";
    printArr(arr, n);

    quickSort(arr, 0, n - 1);  
    cout << "Sorted array: ";
    printArr(arr, n);

    return 0;
}
