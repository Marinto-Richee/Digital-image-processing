# Huffman-Coding
## Aim:
To implement Huffman coding to compress the data using Python.

## Software Required:
1. Anaconda - Python 3.7

## Algorithm:
### Step 1:
Get the input string.

### Step 2:
Create tree nodes

### Step 3:
define the main function to implement huffman coding

### Step 4:
Calculate frequency of occurrence

### Step 5:
Print the characters and its huffmancode
 
 <br><br>
 <br><br>
 <br><br>
 <br><br>
 <br><br>
## Program:
#### Developed By: Marinto Richee
#### Register Number: 212220230031
``` Python
# Get the input String
string=input()
# Create tree nodes
class NodeTree(object):
    def __init__(self,left=None,right=None):
        self.left=left
        self.right=right
    def children(self):
        return(self.left,self.right)
    def  nodes(self):
        return (self.left,self.right)
    def __str__(self):
        return '%s_%s'%(self.left,self.right)

# Main function to implement huffman coding
def huffman_code_tree(node,left=True,binString=''):
    if type(node) is str:
        return {node: binString}
    (l,r)=node.children()
    d=dict()
    d.update(huffman_code_tree(l,True,binString+'0'))
    d.update(huffman_code_tree(r,False,binString+'1'))    
    return d
    
# Calculate frequency of occurrence
freq={}
for c in string:
    if c in freq:
        freq[c]+=1
    else:
        freq[c]=1
freq =sorted(freq.items(),key=lambda x:x[1],reverse=True)
nodes = freq

# Print the characters and its huffmancode
while len(nodes) > 1:
    (key1,c1)=nodes[-1]
    (key2,c2)=nodes[-2]
    nodes=nodes[:-2]
    node=NodeTree(key1,key2)
    nodes.append((node,c1+c2))
    nodes=sorted(nodes,key=lambda x:x[1],reverse=True)

```
## Output:

### Print the characters and its huffmancode

![image](https://user-images.githubusercontent.com/65499285/174433989-d3f5211c-4e55-403b-9cc2-70b16749c81b.png)

![image](https://user-images.githubusercontent.com/65499285/174433983-ac311ac1-7e38-42b1-9d1b-35962f7d754b.png)

## Result
Thus the huffman coding was implemented to compress the data using python programming.
