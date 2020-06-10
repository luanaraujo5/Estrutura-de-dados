from queue import Queue


ROOT = "root"

class Node:
    def __init__(self, data):
        self.data = data
        self.left = None
        self.right = None

    def __str__(self):
        return str(self.data)

class BinaryTree:
    def __init__(self, data=None, node=None):
        if node:
            self.root = node
        elif data: 
            node = Node(data)
            self.root = node
        else:
            self.root = None

class BinarySearchTree(BinaryTree):

    def insert(self, value):
        parent = None
        x = self.root
        while(x):
            parent = x
            if value < x.data:
                x = x.left
            else:
                x = x.right
        if parent is None:
            self.root = Node(value)
        elif value < parent.data:
            parent.left = Node(value)
        else:
            parent.right = Node(value)

    def search (self, value):
        return _search(value, self.root)

    def _search(self, value, node):
        if node is None or node.data==value:
            return BinarySearchTree(node)
            if value < node.data:
                return self._search(value, node.left)
            return self._search(value, node.left)
           
import random
from tree import BinarySearchTree
values = random.sample(range(1,5),5)

bst=BinarySearchTree()

for v in values:
    bst.insert(v)


items = [1, 2, 3, 4, 5]
for item in items:
     r = bst.search(item)
     if r is None:
         print(item, "não encontrado")
     else:
         print(r.root.data, 'encontrado')
