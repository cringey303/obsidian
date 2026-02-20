---
aliases: [Skip List]
tags: [data-structures, EECS330, algorithms, C, Rust]
---
## Overview
Skip lists are randomized data structures built upon sorted linked lists. They achieve the search efficiency of sorted arrays through probabilistic balancing rather than strict tree balancing.

## Time and Space Complexity
| Operation | Average Case | Worst Case |
| :--- | :--- | :--- |
| Search | O(lg n) | O(n) |
| Insert | O(lg n) | O(n) |
| Delete | O(lg n) | O(n) |
| Space | O(n) | O(n lg n) |

*Note: The structure uses a maximum of twice the memory space of a simple doubly linked list.*

## Core Mechanics
1. **Structure**: Maintains multiple sorted linked lists. Elements can appear in multiple lists, connected by vertical links.
2. **Search**: Utilizes upper levels as express routes to skip elements, dropping down a level when the next pointer exceeds the target value.
3. **Insertion**: Elements are always inserted at the bottom list (Level 0).
4. **Promotion**: A fair coin is flipped. If HEAD (50% probability), the element is promoted to the next level up. This repeats until a TAIL occurs or the maximum level is reached.
5. **Deletion**: The target element is removed from all lists that contain it.

## Implementation Details
* **Node Arrays**: Nodes contain an array or vector of forward pointers corresponding to their randomly assigned level.
* **Update Tracker**: Insertion and deletion require an `update` array to track the rightmost nodes visited at each level. This ensures pointers are spliced correctly without breaking the chain.
* **Advantages**: Simpler to implement than balanced trees (like AVL or Red-Black), better memory efficiency, and strong support for concurrency and parallel insertions.
![[Screenshot 2026-02-20 at 10.36.12.png]]