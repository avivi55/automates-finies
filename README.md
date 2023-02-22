# finite-automata-exercises
my school exercises for my finite automata class

---

## TD1

### 1

```mermaid
graph LR
    C((C))
    M((M))
    D((D))
    V((V)) 

    START[ ] --> C 
    C --> STOP[ ]
    M --> STOP2[ ]
    D --> STOP3[ ]
    V--> STOP4[ ]



    C --m--> M
    M --d--> D
    M --v--> V
    D --m--> M
    V --m--> M



    style START height:0px;
    style STOP  height:0px; 
    style STOP2 height:0px;
    style STOP3 height:0px;
    style STOP4 height:0px;
```

### 2

(a)
```mermaid
graph LR
    0((0)) 
    1((1))
    2((2))
    3((3))
    4((4))
    5((5))
    6((6))

    START[ ] --> 0
    6 --> STOP[ ]



    0 --C--> 1
    1 --O--> 2
    2 --U--> 3
    3 --C--> 4
    4 --O--> 5
    5 --U--> 6



    style START height:0px;
    style STOP  height:0px; 
```
</br>
</br>

(b)
```mermaid
graph LR
    0((0)) 
    1((1))
    2((2))
    3((3))

    START[ ] --> 0
    3 --> STOP[ ]



    0 --C--> 1
    1 --O--> 2
    2 --U--> 3
    3 --C--> 1



    style START height:0px;
    style STOP  height:0px; 
```
</br>
</br>
</br>

### 3

(a)
```mermaid
graph LR
    0((0)) 
    1((1))

    START[ ] --> 0
    1 --> STOP[ ]
    
    0 --0--> 1
    1 --1--> 0
    
    0 --1--> 0
    1 --0--> 1



    style START height:0px;
    style STOP  height:0px; 
```
</br>
</br>

(b)
```mermaid
graph LR
    0((0)) 
    1((1))
    2((2))

    START[ ] --> 0 
    2 --> STOP[ ]



    0 --1--> 1 
    1 --1--> 2
    2 --0--> 1    
    1 --0--> 1



    style START height:0px;
    style STOP  height:0px; 
```