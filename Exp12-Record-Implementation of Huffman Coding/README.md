# Huffman Coding
## AIM:
To implement Huffman coding to compress the data using Python.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

## ALGORITHM:
### Step 1:
Get the input string.
### Step 2:
Create tree nodes.
### Step 3:
Define main function to implement Huffman Coding.
### Step 4:
Calculate frequency of occurence.
### Step 5:
Print the characters and it huffman code.

<br><br><br><br><br>

## PROGRAM:
```
/*
Developed by   : Y Chethan
Register Number: 212220230008
*/
```
``` Python
# Get the input String
string='Saveetha Engineering College'

# Create tree nodes
class NodeTree(object):
    def __init__(self,left=None,right=None):
        self.left=left
        self.right=right
        
    def children(self):
        return(self.left,self.right)
    
    def nodes(self):
        return(self.left,self.right)
    
    def __str__(self):
        return '%s_%s' %(self.left,self.right)

# Main function to implement huffman coding
def huffman_code_tree(node,left=True,binString=''):
    if type(node) is str:
        return {node:binString}
    (l,r)=node.children()
    d=dict()
    d.update(huffman_code_tree(l,True,binString+'0'))
    d.update(huffman_code_tree(r,False,binString+'1'))
    return d

# Calculate frequency of occurrence
freq={}
for c in string:
    if c in freq:
        freq[c]=+1
    else:
        freq[c]=1
freq=sorted(freq.items(),key=lambda x:x[1],reverse=True)
nodes=freq
while len(nodes)>1:
    (key1,c1)=nodes[-1]
    (key2,c2)=nodes[-2]
    nodes=nodes[:-2]
    node=NodeTree(key1,key2)
    nodes.append((node,c1+c2))
    nodes=sorted(nodes,key=lambda x:x[1],reverse=True)

# Print the characters and its huffmancode
huffmanCode=huffman_code_tree(nodes[0][0])
print(' Char | Huffman code ')
print('----------------------')
for(char,frequency) in freq:
    print(' %-4r |%12s' % (char,huffmanCode[char]))

```
## OUTPUT:

### Print the characters and its huffmancode
<img width="124" alt="image" src="https://user-images.githubusercontent.com/75234991/174434107-99e1e442-0b8a-4243-8b5d-f4671512a72f.png">

## RESULT:
Thus, the huffman coding was implemented to compress the data using python programming.
