# Master Theorem

> <- Back to [[Recurrence Relations]]

A formula for solving recurrences of the form T(n) = aT(n/b) + O(n^d), which arise in divide-and-conquer algorithms. Compares n^d with n^(log_b(a)) to determine if the work is dominated by the leaves, the root, or distributed evenly. Directly gives the time complexity of merge sort, binary search, and Strassen's algorithm.

#mathematics-for-cs #discrete-mathematics #recurrence-relations #master-theorem
