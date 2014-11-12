##Dynamic Programming
optimization approach that transforms a complex problem into a sequence of simpler problems.

* Longest common subsequence :
 if X(i) = Y(j)
 D(i,j) =D( i-1,j-1 )+ 1
 else :
 D(i,j) =Max(D( i-1,j ),D( i,j-1 ))
 Base cases:
 D( i,0 )=D( 0,j )=0
 
 * minimum number of characters that need to be inserted to make it a palindrome
   1. gap increasing
 	D(i,j)=1+min( D(i+1,j),D(i,j-1) )		if str[i]!=str[j]
 	D(i,j)=D(i+1,j-1)						if str[i]==str[j]
 	
   2.  return string.length()-lcs(string,string.reverse())


* Edit distance:
T(m, n) = T(m-1, n-1) + T(m, n-1) + T(m-1, n) + C

time complexity: O(mn)
space complexity: O(mn)

 Tree Dp :
Problem: given a tree, color nodes black as many as possible without coloring two adjacent nodes
 Subproblems:
 First, we arbitrarily decide the root node 𝑟
 𝐵𝑣: the optimal solution for a subtree having 𝑣 as the root, where we color 𝑣 black
𝑊𝑣: the optimal solution for a subtree having 𝑣 as the root, where we don’t color 𝑣
The answer is max 𝐵𝑟,𝑊𝑟

Base case : Leaf

3. Subset DP :
Prob: given a weighted graph with 𝑛 nodes, find 
the shortest path that visits every node exactly once 
(Traveling Salesman Problem)

Brute force : O(n!)
DP			: O(pow(n,2)*pow(2,n))
D(g,v)=min(D(g-{v},u)+cost(u,v))


 	
