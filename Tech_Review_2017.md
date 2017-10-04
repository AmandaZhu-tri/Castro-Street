# Technical Review Notes
Credits for _Cracking the Code Interview, 6th edition_ and _Data Structure and Algorithms in Python_. 


## Time/Space Complexity

### Big-O, Big-Ω, Big-Θ and Little-O
- T(n) is O(f(n)) = growth rate of T(n) <= growth rate of f(n) _Upper Bound_
- T(n) is Ω(f(n)) = growth rate of T(n) >= growth rate of f(n) _Lower Bound_
- T(n) is Θ(f(n)) = growth rate of T(n) == growth rate of f(n)f(n) _Exact Bound_
- T(n) is o(f(n)) = growth rate of T(n)T(n) < growth rate of f(n)f(n) _Upper Bound that does not equal to_

An __in-place__ algorithm operates directly on its input and changes it, instead of creating and returning a new object. 

## Strings and Arrays

### ASCII and UNICODE 
ASCII defines 128 characters,mapping to 0-127 characters. Unicode defines 2<sup>21</sup> characters.
Unicode is a superset of ASCII, and the numbers 0–128 have the same meaning in ASCII as they have in Unicode.

Because Unicode characters don't generally fit into one 8-bit byte, there are numerous ways of storing Unicode characters in byte sequences, such as UTF-32 and UTF-8.

### Binary Search Trees
- BST Operations are usuallty O(h), h being the height of the tree(length of the path)

#### Red Black Trees
Red Black trees is a balanced Binary Search tree with an extra bit per node-> makes a node either red or black.
- Every node is red or black
- Root is black
- Leaf is black
- If node is red then node is black
- For each node, all simple paths from the node to descendant leaves contain the same number of black nodes.

- By constrainting the node colors on any path frpm the root to a leaf, RBT ensure that no such path is more then twice as ling as another.
- Has height of most 2log(n+1).
- Operations all costs O(log n).
### C++ Review
#### Vector 
* Can change size dynamically.
* Operations: front, back, push_back, pop_back
* vector<int> is non-array, non-reference, and non-pointer - it is being passed by value, and hence it will call copy-    constructor. Must use vector<int>& to pass it as reference.
  
### Other stuff
#### When you type a URL into a web browser, this is what happens:
- If the URL contains a domain name, the browser first connects to a domain name server and retrieves the corresponding IP address for the web server.
- The web browser connects to the web server and sends an HTTP request (via the protocol stack) for the desired web page.
- The web server receives the request and checks for the desired page. If the page exists, the web server sends it. If the server cannot find the requested page, it will send an HTTP 404 error message. 
- The web browser receives the page back and the connection is closed.
- The browser then parses through the page and looks for other page elements it needs to complete the web page. These usually include images, applets, etc.
- For each element needed, the browser makes additional connections and HTTP requests to the server for each element.
- When the browser has finished loading all images, applets, etc. the page will be completely loaded in the browser window.