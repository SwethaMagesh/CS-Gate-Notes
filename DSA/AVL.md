- AVL trees are self-balancing binary search trees.
- In AVL trees, balancing factor of each node is either 0 or 1 or -1.
- Maximum possible number of nodes in AVL tree of height H
= 2<sup>H+1</sup> – 1
- Minimum number of nodes in AVL Tree of height H is given by a recursive relation-
N(H) = N(H-1) + N(H-2) + 1
	- Base conditions for this recursive relation are-

N(0) = 1
N(1) = 2

- Minimum possible height of AVL Tree using N nodes
= ⌊log2N⌋
- Maximum height of AVL Tree using N nodes is calculated using recursive relation-
N(H) = N(H-1) + N(H-2) + 1
	- Base conditions for this recursive relation are-

N(0) = 1
N(1) = 2
- If there are n nodes in AVL Tree, its maximum height can not exceed 1.44log2n.





