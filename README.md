# Selection Sort Algorithm

A simple Python implementation of the **Selection Sort** algorithm.

## 📌 About

Selection Sort is a comparison-based sorting algorithm that repeatedly finds the smallest element from the unsorted portion of a list and swaps it with the first unsorted element.

The algorithm continues this process until the entire list is sorted in ascending order.

## ⚙️ How It Works

For each position in the list:

1. Assume the first unsorted element is the minimum.
2. Search the remaining unsorted portion for a smaller element.
3. Keep track of the index of the smallest element.
4. Swap the smallest element with the first unsorted element.
5. Continue until the list is completely sorted.

The implementation avoids unnecessary swaps when the smallest element is already in the correct position.

## 💻 Implementation

```python
def selection_sort(items):
    for i in range(len(items)):
        min_index = i

        for j in range(i + 1, len(items)):
            if items[j] < items[min_index]:
                min_index = j

        if min_index != i:
            items[i], items[min_index] = items[min_index], items[i]

    return items
