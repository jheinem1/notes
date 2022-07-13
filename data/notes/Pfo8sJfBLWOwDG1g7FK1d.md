Unlike [[ser222.sorting.selection-sort]], Shell Sort has the possibility of $\Omega(n)$ sorting in some cases. It can also have a better average sort time

Although this sort was widely used, this is by-and-large replaced with [[sorting.quick-sort]].

## Steps
1. Perform an [[ser222.sorting.insertion-sort]] starting at the ends of the array, and gradually shrink the internal until it is `1` (i.e., converges to normal insertion sort)
## Implementation
```java
public static void sort(Comparable[] array) {
    int n = a.length;
    int h = 1;
    while (h < N / 3) {
        for (int i = h; i < n; i++)
            for (int j = i; j >= h && less(a[j],a[j - h]); j -= h)
                exch(a, j, j - h);
        h = h / 3;
    }
}
```
## Big-Oh
### Worst-case-scenario
$$
O(n^{\frac32})
$$
### Best-case-scenario
$$
\Omega(n\log{n})
$$