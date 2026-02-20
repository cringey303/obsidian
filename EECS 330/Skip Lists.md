## Overview
* Skip lists are randomized data structures built upon sorted linked lists[cite: 7].
* They achieve the search efficiency of sorted arrays[cite: 7].
* They use probabilistic balancing rather than strictly enforced balancing[cite: 323].

## Complexity
* [cite_start]**Search:** $O(\lg n)$ average case[cite: 317, 318]. [cite_start]$O(n)$ worst case[cite: 9].
* [cite_start]**Insert:** $O(\lg n)$ average case[cite: 317, 318]. [cite_start]$O(n)$ worst case[cite: 9].
* [cite_start]**Delete:** $O(\lg n)$ average case[cite: 317, 318]. [cite_start]$O(n)$ worst case[cite: 9].
* [cite_start]**Memory:** Uses no more than twice the memory space compared to simple doubly linked lists[cite: 128].

## Architecture
* [cite_start]Maintains multiple sorted lists[cite: 36].
* [cite_start]Elements can appear in more than one list[cite: 36].
* [cite_start]Vertical links connect elements across lists[cite: 36].
* [cite_start]Functions similarly to express trains skipping stations[cite: 37].


## Core Operations

### Search
* [cite_start]Maintain $\lg n$ sorted lists[cite: 114].
* [cite_start]Search at most 2 elements per list[cite: 126].
* [cite_start]Cost is $2 \lg n$[cite: 115].


### Insert
* [cite_start]Search to find the correct insertion point[cite: 205].
* [cite_start]Always insert the element into the bottom list first[cite: 205].
* [cite_start]Flip a fair coin to decide promotion[cite: 238].
* [cite_start]A HEAD outcome (50% probability) promotes the element to the next level up[cite: 237].


### Delete
* Locate the element.
* [cite_start]Delete it from all lists containing it[cite: 177].

## Advantages Over Balanced Trees
* [cite_start]Simpler implementation compared to AVL or red-black trees[cite: 10, 12].
* [cite_start]Supports concurrency, including parallel inserts[cite: 13].
* [cite_start]Faster search and query operations[cite: 14, 324].
* [cite_start]Better memory efficiency[cite: 15].

## Background
* [cite_start]Invented by William Pugh in 1989[cite: 320].
* [cite_start]Used in production systems like the Apache runtime and Redis[cite: 321].