# MA3 - Sorting Algorithm Comparison

# Performance Comparison (10 Trials Each)
Insertion Sort
Avg Time: 81.85 ms
Std Dev: 0.76 ms

Quick Sort
Avg Time: 1.22 ms
Std Dev: 0.06 ms

Shell Sort
Avg Time: 1.88 ms
Std Dev: 0.03 ms

Heap Sort
Avg Time: 2.15 ms
Std Dev: 0.02 ms

# Observations & Comparison

Quick sort was by far the fastest out of all four algorithms. It consistently stayed around 1.2 ms with barely any fluctuation. Shell sort came in second, averaging around 1.88 ms, followed by heap sort at 2.15 ms. Insertion sort was way slower — almost 82 ms on average — so it clearly doesn't scale well with larger inputs.

## Why Quick Sort Wins

Quick sort outperforms the others here because it’s a divide-and-conquer algorithm that uses in-place partitioning. Since the data is randomly distributed and we’re using the last element as the pivot, it doesn’t run into worst-case behavior often. It’s efficient and has low overhead, which is why it crushed the other sorts in every trial.

# Shell Sort Gap Sequence

I experimented with a few gap sequences including:
`N / 2, N / 4, .. 1`  (simple divide-by-2)
`N / 2.2, N / 2.2^2, ...`  (Sedgewick-like)

In the end, I stuck with the classic `gap /= 2` approach because it was clean, performed well, and didn't add complexity. It stayed very stable across trials and gave solid middle-ground performance between quicksort and heap sort.
