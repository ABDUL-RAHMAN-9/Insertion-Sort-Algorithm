# Insertion-Sort-Algorithm

* Insertion sort is a simple sorting algorithm that works by iteratively inserting each element of an unsorted list into its correct position in a sorted portion of the list. It is like sorting playing cards in your hands. You split the cards into two groups: the sorted cards and the unsorted cards. Then, you pick a card from the unsorted group and put it in the right place in the sorted group.

1.We start with the second element of the array as the first element is assumed to be sorted.

2.Compare the second element with the first element if the second element is smaller then swap them.

3.Move to the third element, compare it with the first two elements, and put it in its correct position.

4.Repeat until the entire array is sorted.

# Steps:
<div align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20250322120814021166/Insertion-Sort--1.webp" width="400">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20250322120813676040/Insertion-Sort--2.webp" width="400">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20250322120813423266/Insertion-Sort--3.webp" width="400">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20250322120812765435/Insertion-Sort--4.webp" width="400">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20250322120812115216/Insertion-Sort--5.webp" width="400">
</div>

# Code:

```
// C++ program for implementation of Insertion Sort
#include <iostream>
using namespace std;

/* Function to sort array using insertion sort */
void insertionSort(int arr[], int n)
{
    for (int i = 1; i < n; ++i) {
        int key = arr[i];
        int j = i - 1;

        /* Move elements of arr[0..i-1], that are
           greater than key, to one position ahead
           of their current position */
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key;
    }
}

/* A utility function to print array of size n */
void printArray(int arr[], int n)
{
    for (int i = 0; i < n; ++i)
        cout << arr[i] << " ";
    cout << endl;
}

// Driver method
int main()
{
    int arr[] = { 12, 11, 13, 5, 6 };
    int n = sizeof(arr) / sizeof(arr[0]);

    insertionSort(arr, n);
    printArray(arr, n);

    return 0;
}

```
# Output:

```
5 6 11 12 13 
```
# Illustration:

<div align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240802210251/Insertion-sorting.png" width="400">
</div>


# Complexity Analysis:
- Time Complexity: O(n²)
- Space Complexity: O(1)




