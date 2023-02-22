# finite-automata-exercises
my school exercises for my finite automata class

---

## TD1

### 1

```mermaid
graph LR
    style ENTREE height:0px;
    style SORTIE  height:0px; 
    style SORTIE2 height:0px;
    style SORTIE3 height:0px;
    style SORTIE4 height:0px;
    
    C((C))
    M((M))
    D((D))  
    V((V)) 

    ENTREE[ ] --> C 
    C --> SORTIE[ ]
    M --> SORTIE2[ ]
    D --> SORTIE3[ ]
    V--> SORTIE4[ ]



    C --m--> M
    M --d--> D
    M --v--> V
    D --m--> M
    V --m--> M
```

### 2

$a)$
```mermaid
graph LR
    style ENTREE height:0px;
    style SORTIE  height:0px; 

    0((0)) 
    1((1))
    2((2))
    3((3))
    4((4))
    5((5))
    6((6))

    ENTREE[ ] --> 0
    6 --> SORTIE[ ]



    0 --C--> 1
    1 --O--> 2
    2 --U--> 3
    3 --C--> 4
    4 --O--> 5
    5 --U--> 6
```
</br>
</br>

$b)$
```mermaid
graph LR
    style ENTREE height:0px;
    style SORTIE  height:0px;

    0((0)) 
    1((1))
    2((2))
    3((3))

    ENTREE[ ] --> 0
    3 --> SORTIE[ ]



    0 --C--> 1
    1 --O--> 2
    2 --U--> 3
    3 --C--> 1 
```
</br>
</br>
</br>

### 3

$a)$
```mermaid
graph LR
    style ENTREE height:0px;
    style SORTIE  height:0px; 
    
    0((0)) 
    1((1))

    ENTREE[ ] --> 0
    1 --> SORTIE[ ]
    
    0 --0--> 1
    1 --1--> 0
    
    0 --1--> 0
    1 --0--> 1
```
</br>
</br>

$b)$
```mermaid
graph LR
    style ENTREE height:0px;
    style SORTIE  height:0px; 
    
    0((0)) 
    1((1))
    2((2))

    ENTREE[ ] --> 0 
    2 --> SORTIE[ ]



    0 --1--> 1 
    1 --1--> 2
    2 --0--> 1    
    1 --0--> 1
```
</br>
</br>


Soit P = point( . )

$c)$
```mermaid
graph LR
    style ENTREE height:0px;
    style ENTREE2 height:0px;
    style SORTIE  height:0px; 
    style SORTIE2  height:0px; 

    0((0)) 
    1((1))
    2((2))
    3((3))
    4((4))

    ENTREE[ ] --> 0 
    ENTREE2[ ] --> 1
    3 --> SORTIE[ ]
    4 --> SORTIE2[ ]



    0 -- +/- --> 1 

    1 -- 0..9  --> 2
    1 -- P --> 3    
    
    2 -- P --> 4

    3 -- 0..9 --> 3
    3 -- 0..9 --> 4

    4 -- 0..9 --> 4
```
</br>
</br>


$d)$
```mermaid
graph LR
    style ENTREE height:0px;
    style SORTIE  height:0px; 
    
    0((0)) 
    1((1))
    2((2))
    3((3))
    4((4))
    5((5))

    
    ENTREE[ ] --> 0 
    5 --> SORTIE[ ]



    0 --0--> 1 
    0 --1--> 2 

    1 --0--> 1
    1 --1--> 3    

    3 --0--> 5
    3 --1--> 3
    
    2 --1--> 2
    2 --0--> 4

    4 --0--> 4
    4 --1--> 5
```
</br>
</br>


$e)$
```mermaid
graph LR
    style ENTREE height:0px;
    style SORTIE  height:0px; 
    style SORTIE2  height:0px;  

    0((0)) 
    1((1))
    2((2))
    3((3))

    ENTREE[ ] --> 0
    3 --> SORTIE2[ ]
    1 --> SORTIE[ ]


    0 --a--> 1 
    0 --b--> 3 
    1 --a--> 0
    1 --b--> 2    
    2 --b--> 3
    3 --b--> 2  
```
</br>
</br>
</br>


### 4

**Méthode de cours :**

| 7n % 7 | 14n % 7 | 14n+1 % 7 |
|:------:|:-------:|:---------:|
|        |    0    |     1     |
|        |         |           |
|    0   |    0    |     1     |
|    1   |    2    |     3     |
|    2   |    4    |     5     |
|    3   |    6    |     0     |
|    4   |    1    |     2     |
|    5   |    3    |     4     |
|    6   |    5    |     6     |

<br>

Tableau de transition :
| État |  0  |  1  |
|:----:|:---:|:---:|
|   0  |  0  |  1  |
|   1  |  2  |  3  |
|   2  |  4  |  5  |
|   3  |  6  |  0  |
|   4  |  1  |  2  |
|   5  |  3  |  4  |
|   6  |  5  |  6  |

```mermaid
graph LR
    style ENTREE height:0px;
    style SORTIE  height:0px; 

    0((0)) 
    1((1))
    2((2))
    3((3))
    4((4))
    5((5))
    6((6))

    ENTREE[ ] --> 0
    6 --> SORTIE[ ]


    0 --0--> 0
    0 --1--> 1

    1 --0--> 2
    1 --1--> 3
    
    2 --0--> 4
    2 --1--> 5
    
    3 --0--> 6
    3 --1--> 0 

    4 --0--> 1
    4 --1--> 2
    
    5 --0--> 3
    5 --1--> 4
    
    6 --1--> 6
    6 --0--> 5
```
</br>
</br>
</br>


### 5

$a)$

Les mots reconnus par l'automate (chemin inverse):
{
    a,
    ab,
    bab,
    abbb,
    bbba,
    ...
}

Soit $B$ = $n$ $\cdot$ b, $n \in \mathbb{N^+}$

Donc l'automate reconnait les mots de la formes :  $B$ a $B$


Les états **1** et **3** sont inutile car inatteignable ou ne menant à rien.
</br>
</br>
</br>


### 6

Toutes les sous-questions
$a)$ ont comme réponse : `non standard`

Nous étudieront donc que les sous-questions $b)$ et $c)$

Nous nous permettrons de compléter les automates au besoin.

$6.1)$
```mermaid
graph LR
    style ENTREE height:0px;
    style SORTIE  height:0px; 

    1((1))

    ENTREE[ ] --> 1
    1 --> SORTIE[ ]



    1 --a--> 1
```

$b)$
```mermaid
graph LR
    style ENTREE height:0px;
    style SORTIE  height:0px; 
    style SORTIE2  height:0px; 

    I((I)) 
    1((1))

    ENTREE[ ] --> I --> SORTIE2[ ]
    1 --> SORTIE[ ]


    I --a--> 1
    1 --a--> 1
```
$c)$
```mermaid
graph LR
    style ENTREE height:0px;
    style SORTIE  height:0px; 

    I((I)) 
    1((1))

    ENTREE[ ] --> I
    1 --> SORTIE[ ]


    I --a--> 1
    1 --a--> 1
```

<br>
<br>

$6.2)$
```mermaid
graph LR
    style ENTREE height:0px;
    style SORTIE  height:0px; 

    1((1))
    2((2))

    ENTREE[ ] --> 1
    2 --> SORTIE[ ]



    1 --a--> 2
    2 --b--> 1
```

$b)$
```mermaid
graph LR
    style ENTREE height:0px;
    style SORTIE  height:0px; 

    I((I)) 
    1((1))
    2((2))

    ENTREE[ ] --> I
    2 --> SORTIE[ ]



    I --a--> 1 

    1 --a--> 2
    2 --b--> 1 
```
$c)$ Il ne reconnaît pas le mot vide.

<br>
<br>

$6.3)$
```mermaid
graph LR
    style ENTREE height:0px;
    style SORTIE  height:0px; 
    style SORTIE2  height:0px; 

    1((1))
    2((2))

    ENTREE[ ] --> 1 --> SORTIE2[ ]
    2 --> SORTIE[ ]



    1 --a--> 2
    2 --b--> 1
```

$b)$
```mermaid
graph LR
    style ENTREE height:0px;
    style SORTIE  height:0px; 
    style SORTIE2  height:0px; 

    I((I)) 
    1((1))
    2((2))

    ENTREE[ ] --> I --> SORTIE2[ ]
    2 --> SORTIE[ ]



    I --a--> 2 

    1 --a--> 2
    2 --b--> 1 
```
$c)$
```mermaid
graph LR
    style ENTREE height:0px;
    style SORTIE  height:0px; 

    I((I)) 
    1((1))
    2((2))

    ENTREE[ ] --> I
    2 --> SORTIE[ ]



    I --a--> 2 

    1 --a--> 2
    2 --b--> 1 
```

