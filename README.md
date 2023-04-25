# -Selection-Sorting-technique
Selection sort is a straightforward sorting algorithm that sorts an array by continually selecting the smallest element from the array's unsorted portion and inserting it at the start of the array's sorted portion. In both the best and worst scenarios, it has a time complexity of O(n^2).

The method of selection sort divides the array into two halves, one of which will be sorted and the other of which will not. We will choose one element from the unsorted section of the array and add it to the sorted part of the array after each step in the selection sort algorithm.

In essence, it chooses the smallest member from the array's unsorted section and swaps it with the last index of the sorted section. Up until the entire array is sorted in either ascending or descending order, the procedure of selecting the smallest element in the array from the unsorted portion of the array and replacing it with an element of the sorted section is repeated.

Code-

        #include <stdio.h>

        void Selectionsort(int a[], int n)
        {
            int i, j, smallest, temp;
            for (i = 0; i < n - 1; i++)
            {
                smallest = i;
                for (j = i + 1; j < n; j++)
                {
                    if (a[smallest] > a[j])
                    {
                        smallest = j;
                    }
                }
                if (i != smallest)
                {
                    temp = a[i];
                    a[i] = a[smallest];
                    a[smallest] = temp;
                }
            }
            printf("%d %d %d %d %d", a[0], a[1], a[2], a[3], a[4]);
        }

        int main()
        {
            int array[5] = {23, 45, 65, 7, 5};
            Selectionsort(array, 5);
            return 0;
        }
        
 Explanation:

An integer array of type a and its size, n, are input arguments for the selectionsort function. The array is then subjected to selection sorting by locating the smallest element in the remaining unsorted portion of the array after iterating through each element in the array. The index of the smallest element discovered is tracked by the smallest variable. The function switches the items at the ith position and the smallest location in the array if the smallest element is not already in its proper place.

The sorted array is lastly printed by the Selectionsort function's printf instruction.

An integer array array of size 5 is declared and initialised with 5 unsorted integers in the main function. The array and its size are then sent as parameters to the Selectionsort method. When the function is finished, main returns 0, indicating that the programme has been successfully run.

The output of the programme will show the sorted array as "5 7 23 45 65" once it has run.

![Screenshot (734)](https://user-images.githubusercontent.com/91966097/234368618-199f67e4-a2f4-403e-85b7-6a7a9f34073a.png)

