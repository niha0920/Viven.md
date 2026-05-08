# 2d_array.c
```c
#include<stdio.h>
#include<stdlib.h>
#define rows 3
#define cols 3
int main()
{
        int **arr = (int **)malloc(rows * sizeof(int *));
        for(int i = 0; i < rows; i++)
        {
                arr[i] = (int *)malloc(cols * sizeof(int));
        }
        for(int i = 0;i < rows; i++)
        {
                for(int j = 0; j < cols; j++)
                {
                        scanf("%d", &arr[i][j]);
                }
        }
        for(int i = 0; i < rows; i++)
        {
                for(int j = 0; j < cols; j++)
                {
                        printf("%d ", arr[i][j]);
                }
                printf("\n");
        }
        for(int i = 0; i < rows; i++)
        {
                free(arr[i]);
        }
        free(arr);
}
```

# dynamic_2d_array.c
```c
#include<stdio.h>
#include<stdlib.h>
#define rows 3
#define cols 3
int main()
{
        int *arr = (int *)malloc(rows * cols * sizeof(int));
        for(int i = 0; i < rows; i++)
        {
                for(int j = 0; j < cols; j++)
                {
                        scanf("%d", &arr[i * cols + j]);
                }
        }
        for(int i = 0; i < rows; i++)
        {
                for(int j = 0; j < cols; j++)
                {
                        printf("%d ", arr[i * cols + j]);
                }
                printf("\n");
        }
        free(arr);
}
```

# binary_search.c
```c
#include<stdio.h>
int binarySearch(int arr[], int len, int key)
{
        int left = 0;
        int right = len - 1;
        while(left <= right)
        {
                int mid = (left + right) / 2;
                if(arr[mid] ==  key)
                        return mid;
                else if(arr[mid] > key)
                        right = mid - 1;
                else
                        left = mid + 1;
        }
        return -1;
}
int main()
{
        int arr[] = {1, 2, 3, 4, 5, 6, 7, 8, 9};
        int len = sizeof(arr) / sizeof(arr[0]);
        int key = 3;
        int index = binarySearch(arr, len, key);
        if(index != -1)
                printf("%d at index %d", key, index);
        else
                printf("Not found");
}
```

# freq_elements.c
```c
#include<stdio.h>
int main()
{
        int arr[] = {1,2,3,1,2,3,5,5,4,3};
        int n = sizeof(arr) / sizeof(arr[0]);
        int freq[256] = {0};
        for(int i = 0; i < n; i++)
        {
                freq[arr[i]]++;
        }
        for(int i = 0; i < 256; i++)
        {
                if(freq[i] > 0)
                        printf("%d -> %d times\n", i, freq[i]);
        }
}
```

# large_sec_largest.c
```c
#include<stdio.h>
#include<limits.h>
int main()
{
        int arr[] = {1,2,10,5,7,12};
        int n = sizeof(arr) / sizeof(arr[0]);
        int max1 = INT_MIN, max2 = INT_MIN;
        for(int i = 0; i < n; i++)
        {
                if(arr[i] > max1)
                {
                        max2 = max1;
                        max1 = arr[i];
                }
                else if(arr[i] < max1 && arr[i] > max2)
                        max2 = arr[i];
        }
        printf("Second largest element: %d", max2);
}
```

# largest_smallest.c
```c
#include<stdio.h>
int main()
{
        int arr[] = {2,3,4,15,6,5};
        int n = sizeof(arr) / sizeof(arr[0]);
        int large = arr[0];
        int small = arr[0];
        for(int i = 0; i < n; i++)
        {
                if(arr[i] > large)
                        large = arr[i];
                if(arr[i] < small)
                        small = arr[i];
        }
        printf("Large: %d Small: %d", large, small);
}
```

# merge_sorted_arrays.c
```c
#include<stdio.h>
#define size 3
int main()
{
        int arr1[size] = {1, 2, 3};
        int arr2[size] = {3, 4, 5};
        int arr3[size + size];
        for(int i = 0; i < size; i++)
        {
                arr3[i] = arr1[i];
                arr3[size + i] = arr2[i];
        }
        for(int i = 0; i < (size + size); i++)
        {
                printf("%d ", arr3[i]);
        }
}
```
