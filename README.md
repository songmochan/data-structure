1.
class CompleteBinary Tree:
def_init_(self):
  self.root = None
def parent(self,i):
  if i == 0:
     return None
  else:
     return(-1)//2
def left_child(self,i):
  return 2*1+1
def right_child(self,i):
  return 2*i+2
 
2.
def_init_(self):
  self.tree = CompleteBinaryTree()
  self.size = 0
def insert(self,key):
#create a new node and add it to the end of the list
new_node = Node(key)
if self.tree.root is None:
   self.tree.root = new_node
else:
   current = self.tree.root
   while current.next is not None:
     current = current.next
   current.next = new_node
self.size +=1
i = self.size-1
while i > 0 and self.tree.get_node_value(self.tree.parent(i)) > self.tree.get_node_value(i):
  self.tree.swap(i, self.tree.parent(i))
  i = self.tree.parent(i)
def delMin(self):
  if self.size == 0:
     return None
  min_key = self.tree.get_node_value(0)
  self.tree.set_node_value(0,self.tree.get_node_value(self.size-1))
  self.size-=1
  i = o
  while i < self.size
    left_child = self.tree.left_child(i)
    right_child = self.tree.right_child(i)
    min_child = i
    if left_child < self.size and self.tree.get_node_value(left_child) < self.tree.get_node_value(min_child):
       min_child = left_child
    if right_child < self.size and self.tree.get_node_value(right_child) < self.tree.get_node_value(min_child):
       min_child = right_child
    if min_child != i:
       self.tree.swap(i, min_child)
       i = min_child
    else:
       break
return min_key

insert(key): This method takes a key as an argument and creates a new node with the given key. It adds the node to the end of the linked list and increases the size of the tree. It then uses a while loop to compare the value of the new node with that of its parent, swapping them if the new node has a smaller value. This process is called "bubbling" so that the new node will be placed in the correct location according to its value. 
delMin(): This method removes the minimum key from the priority queue. If the size of the tree is 0, None is returned. Otherwise, it removes the smallest key from the root (the first node in the linked list) and sets the value of the last node to root. It then uses a while loop to compare the values of the new root node and its left and right child nodes, swapping with the smallest child node if necessary. This process is called "bubbling down" so that the new root will be placed in the correct position according to its value. The method continues the process until the new root is in the correct location. This ensures that the minimum key is always at the root of the tree and can be easily removed. Finally, the method returns the minimum key that was removed from the root node. It is important to note that the size of the tree is decreasing in the first step so that the last element in the tree can be used to replace the root element. This ensures that the tree remains a full binary tree and that the minimum heap property is maintained. It is also important to note that the implementation of the priority queue is based on a complete binary tree. This is not a general implementation, it is just a specialization of a binary tree with specific properties.

3.
insert(): The insert method first adds a new node to the end of the linked list, which takes O(n) time, where n is the number of nodes in the tree. Then, it performs the "bubbling up" operation, which is O(log n) in the average case and O(n) in the worst case. The worst case occurs when the tree is not a complete binary tree, and the new node needs to be moved all the way up to the root. In this case, the overall time complexity of the insert method is O(n + log n) = O(n).
delMin(): The delMin method first removes the root node from the tree, which takes O(1) time. Then, it performs the "bubbling down" operation, which is also O(log n) in the average case and O(n) in the worst case. The worst case occurs when the tree is not a complete binary tree and the new root needs to be moved all the way down to a leaf node. In this case, the overall time complexity of the delMin method is O(1 + log n) = O(log n).
