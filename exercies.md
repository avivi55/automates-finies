# Exerices Automates Finis
---

## Sommaire

* [TD1](#-td1)

---

$
%  MACROS
\gdef\EX#1{\huge{\text{Exercice #1}}}
$


## TD1

<br>
<br>

$$\EX{1}$$

!!! quote ""
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
<br>
<br>
<br>
<br>
<br>
<br>

$$\EX{2}$$

$a)$

!!! quote ""
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

$b)$ Standardisation

!!! quote ""
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

<br>
<br>
<br>
<br>
<br>
<br>

$$\EX{3}$$

$a)$

!!! quote ""
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

$b)$ Standardisation

!!! quote ""
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


$c)$
$Soit$ P = $\cdot$

!!! quote ""
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

$d)$

!!! quote ""
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

$e)$

!!! quote ""
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

<br>
<br>
<br>
<br>
<br>
<br>

$$\EX{4}$$

**Méthode de cours :**

| 7n % 7 | 14n % 7 | 14n+1 % 7 |
|:------:|:-------:|:---------:|
|        |    0    |     1     |
|    ^   |    >    |     -     |
|    0   |    0    |     1     |
|    1   |    2    |     3     |
|    2   |    4    |     5     |
|    3   |    6    |     0     |
|    4   |    1    |     2     |
|    5   |    3    |     4     |
|    6   |    5    |     6     |

<br>

!!! quote ""
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

<br>
<br>
<br>
<br>
<br>
<br>

$$\EX{5}$$


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
Les états $\textcircled{1}$ et $\textcircled{3}$ sont inutile car inatteignable ou ne menant à rien.

<br>
<br>
<br>
<br>
<br>
<br>

$$\EX{6}$$


!!! info ""
    Toutes les sous-questions $a)$ ont comme réponse : `non standard` 
    Nous étudieront donc que les sous-questions $b)$ et $c)$

$6.1)$


!!! quote ""
    ```mermaid
    graph LR
        style ENTREE height:0px;
        style SORTIE  height:0px; 

        1((1))

        ENTREE[ ] --> 1
        1 --> SORTIE[ ]



        1 --a--> 1
    ```

$b)$ Standardisation

!!! quote ""
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

!!! quote ""
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

!!! quote ""
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

$b)$ Standardisation

!!! quote ""
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

!!! quote ""
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

$b)$ Standardisation

!!! quote ""
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

!!! quote ""
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

<br>
<br>

$6.4)$

!!! quote ""
    ```mermaid
    graph LR
        style ENTREE height:0px;
        style SORTIE  height:0px; 
        style SORTIE2  height:0px; 

        1((1))
        2((2))
        3((3))

        ENTREE[ ] --> 1 
        2 --> SORTIE[ ]
        3 --> SORTIE2[ ]



        1 --a--> 1
        1 --a--> 3
        1 --b--> 2
        
        2 --a--> 1
        2 --b--> 3
    ```

###### $b)$ Standardisation

!!! quote ""
    ```mermaid
    graph LR
        style ENTREE height:0px;
        style SORTIE2  height:0px; 
        style SORTIE3  height:0px; 

        I((I)) 
        1((1))
        2((2))
        3((3))

        ENTREE[ ] --> I
        2 --> SORTIE2[ ]
        3 --> SORTIE3[ ]



        I --a--> 1
        I --a--> 3
        I --b--> 2

        1 --a--> 1
        1 --a--> 3
        1 --b--> 2
        
        2 --a--> 1
        2 --b--> 3
    ```

$c)$ Il ne reconnaît pas le mot vide.

<br>
<br>

$6.5)$

!!! quote ""
    ```mermaid
    graph LR
        style ENTREE height:0px;
        style ENTREE2 height:0px;
        style SORTIE  height:0px; 
        style SORTIE2  height:0px; 

        1((1))
        2((2))
        3((3))

        ENTREE[ ] --> 1 
        ENTREE2[ ] --> 3
        2 --> SORTIE[ ]
        3 --> SORTIE2[ ]



        1 --a--> 1
        1 --a--> 3
        1 --b--> 2
        
        2 --a--> 1
        2 --b--> 3
    ```

$b)$ Standardisation

!!! quote ""
    ```mermaid
    graph LR
        style ENTREE height:0px;
        style SORTIE  height:0px; 
        style SORTIE2  height:0px; 
        style SORTIE3  height:0px; 

        I((I)) 
        1((1))
        2((2))
        3((3))

        ENTREE[ ] --> I --> SORTIE[ ]
        2 --> SORTIE2[ ]
        3 --> SORTIE3[ ]



        I --a--> 1
        I --a--> 3
        I --b--> 2

        1 --a--> 1
        1 --a--> 3
        1 --b--> 2
        
        2 --a--> 1
        2 --b--> 3
    ```

$c)$
[$cf.~~6.4)~b)$](#-b-standardisation)

<br>
<br>

$6.6)$

!!! quote ""
    ```mermaid
    graph LR
        style ENTREE height:0px;
        style ENTREE2 height:0px;
        style SORTIE  height:0px; 
        style SORTIE2  height:0px; 

        1((1))
        2((2))
        3((3))
        4((4))

        ENTREE[ ] --> 1 
        ENTREE2[ ] --> 3 
        2 --> SORTIE[ ]
        4 --> SORTIE2[ ]


        4 --b--> 3

        3 --a--> 2
        3 --a--> 4

        1 --a--> 2
        1 --b--> 4
    ```

###### $b)$ Standardisation (2)

!!! quote ""
    ```mermaid
    graph LR
        style ENTREE height:0px;
        style SORTIE  height:0px; 
        style SORTIE2  height:0px; 

        I((I)) 
        1((1))
        2((2))
        3((3))
        4((4))

        ENTREE[ ] --> I
        4 --> SORTIE[ ]
        2 --> SORTIE2[ ]



        I --a--> 2
        I --a/b--> 4

        4 --b--> 3

        3 --a--> 2
        3 --a--> 4

        1 --a--> 2
        1 --b--> 4
    ```

$c)$ Il ne reconnaît pas le mot vide.

<br>
<br>

$6.7)$

!!! quote ""
    ```mermaid
    graph LR
        style ENTREE height:0px;
        style ENTREE2 height:0px;
        style SORTIE  height:0px; 
        style SORTIE2  height:0px; 
        style SORTIE3  height:0px; 

        1((1))
        2((2))
        3((3))
        4((4))

        ENTREE[ ] --> 1 
        ENTREE2[ ] --> 3 
        2 --> SORTIE[ ]
        4 --> SORTIE2[ ]
        3 --> SORTIE3[ ]


        4 --b--> 3

        3 --a--> 2
        3 --a--> 4

        1 --a--> 2
        1 --b--> 4
    ```

$b)$ Standardisation

!!! quote ""
    ```mermaid
    graph LR
        style ENTREE height:0px;
        style SORTIE  height:0px; 
        style SORTIE2  height:0px; 
        style SORTIE3  height:0px; 

        I((I)) 
        1((1))
        2((2))
        3((3))
        4((4))

        ENTREE[ ] --> I --> SORTIE3[ ]
        4 --> SORTIE[ ]
        2 --> SORTIE2[ ]



        I --a--> 2
        I --a/b--> 4

        4 --b--> 3

        3 --a--> 2
        3 --a--> 4

        1 --a--> 2
        1 --b--> 4
    ```

$c)$
[$cf.~~6.6)~b)$](#-b-standardisation-2)

<br>
<br>
<br>
<br>
<br>
<br>

$$\EX{7}$$

$\text{Automate A :}$

!!! quote ""
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



        0 --a/b--> 0
        0 --b--> 1

        1 --a--> 2
        
        2 --b--> 3
    ```

Le langage reconnu est : les mots finissant par $bab$

Nous construisons le tableau de déterminisation : 

| $E/S$ |  .  |  a  |   b  |
|:-----:|:---:|:---:|:----:|
|  $E$  |  0  |  0  | 0, 1 |
|       |  1  |  2  |   .  |
|   ^   |  2  |  .  |   3  |
|  $S$  |  3  |  .  |   .  |

Le tableau déterminisé donne :

| $E/S$ |  .  |  a  |  b  |
|:-----:|:---:|:---:|:---:|
|  $E$  |  0  |  0  |  01 |
|       |  01 |  02 |  01 |
|   ^   |  02 |  0  | 013 |
|  $S$  | 013 |  02 |  01 |

<br>
<br>

$\text{Automate B :}$

!!! quote ""
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



        0 --a/b--> 0
        0 --b--> 1

        1 --a--> 2
        
        2 --a/b--> 3
    ```

Le langage reconnu est : les mots finissant par $ba(a\text{ ou }b)$

Nous construisons le tableau de déterminisation : 

| $E/S$ |  .  |  a  |   b  |
|:-----:|:---:|:---:|:----:|
|  $E$  |  0  |  0  | 0, 1 |
|       |  1  |  2  |   .  |
|   ^   |  2  |  3  |   3  |
|  $S$  |  3  |  .  |   .  |

Le tableau déterminisé donne :

| $E/S$ |  .  |  a  |  b  |
|:-----:|:---:|:---:|:---:|
|  $E$  |  0  |  0  |  01 |
|       |  01 |  02 |  01 |
|   ^   |  02 |  03 | 013 |
|   ^   |  03 |  0  |  01 |
|  $S$  | 013 |  02 |  01 |

<br>
<br>

$\text{Automate C1 :}$

!!! quote ""
    ```mermaid
    graph LR
        style ENTREE height:0px;
        style ENTREE2 height:0px;
        style SORTIE  height:0px; 
        style SORTIE2  height:0px; 

        0((0))
        2((2))
        1((1))
        3((3))

        ENTREE[ ] --> 0 
        ENTREE2[ ] --> 2
        1 --> SORTIE[ ]
        3 --> SORTIE2[ ]



        2 --a--> 3
        
        1 --b--> 2
        
        0 --a--> 1   
    ```

Le langage reconnu est : les mots tels que $\in \{a, aba\}$

Nous construisons le tableau de déterminisation : 

| $E/S$ |  .  |  a  |  b  |
|:-----:|:---:|:---:|:---:|
|  $E$  |  0  |  1  |  .  |
|  $S$  |  1  |  .  |  2  |
|  $E$  |  2  |  3  |  .  |
|  $S$  |  3  |  .  |  .  |

Le tableau déterminisé donne :

| $E/S$ |  .  |  a  |  b  |
|:-----:|:---:|:---:|:---:|
|  $E$  |  02 |  13 | $P$ |
|  $S$  |  13 | $P$ |  2  |
|       |  2  |  3  | $P$ |
|  $S$  |  3  | $P$ | $P$ |
|       | $P$ | $P$ | $P$ |

<br>
<br>

$\text{Automate C2 :}$

!!! quote ""
    ```mermaid
    graph LR
        style ENTREE height:0px;
        style ENTREE2 height:0px;
        style SORTIE  height:0px; 
        style SORTIE2  height:0px; 

        0((0))
        2((2))
        1((1))
        3((3))

        ENTREE[ ] --> 0 
        ENTREE2[ ] --> 2
        1 --> SORTIE[ ]
        3 --> SORTIE2[ ]



        0 --a--> 1   
        2 --b--> 3    
    ```

Le langage reconnu est : $a\text{ ou }b$

Nous construisons le tableau de déterminisation : 

| $E/S$ |  .  |  a  |  b  |
|:-----:|:---:|:---:|:---:|
|  $E$  |  0  |  1  |  .  |
|  $E$  |  2  |  .  |  3  |
|  $S$  |  1  |  .  |  .  |
|  $S$  |  3  |  .  |  .  |

Le tableau déterminisé donne :

| $E/S$ |  .  |  a  |  b  |
|:-----:|:---:|:---:|:---:|
|  $E$  |  02 |  1  |  3  |
|  $S$  |  1  | $P$ | $P$ |
|  $S$  |  3  | $P$ | $P$ |
|       | $P$ | $P$ | $P$ |

<br>
<br>

$\text{Automate C3 :}$

!!! quote ""
    ```mermaid
    graph LR
        style ENTREE height:0px;
        style ENTREE2 height:0px;
        style SORTIE  height:0px; 
        style SORTIE2  height:0px; 

        0((0))
        2((2))
        1((1))
        3((3))

        ENTREE[ ] --> 0 
        ENTREE2[ ] --> 2
        1 --> SORTIE[ ]
        3 --> SORTIE2[ ]



        0 --a--> 1   
        2 --a--> 3    
    ```

Le langage reconnu est : $a$

Nous construisons le tableau de déterminisation : 

| $E/S$ |  .  |  a  |  b  |
|:-----:|:---:|:---:|:---:|
|  $E$  |  0  |  1  |  .  |
|  $S$  |  1  |  .  |  .  |
|  $E$  |  2  |  3  |  .  |
|  $S$  |  3  |  .  |  .  |

Le tableau déterminisé donne :

| $E/S$ |  .  |  a  |  b  |
|:-----:|:---:|:---:|:---:|
|  $E$  |  02 |  13 | $P$ |
|  $S$  |  13 | $P$ | $P$ |
|       | $P$ | $P$ | $P$ |

<br>
<br>

$\text{Automate D :}$

!!! quote ""
    ```mermaid
    graph LR
        style ENTREE height:0px;
        style SORTIE  height:0px; 

        A((A))
        B((B))
        C((C))

        ENTREE[ ] --> A
        B --> SORTIE[ ]



        A --a--> A
        A --a, b--> B
        
        B --a, b--> C
        
        C --a, b--> C
    ```

Le langage reconnu est : les mots tels que 
$n*a$ et finissant par $a\text{ ou }b$ $,~n \in \mathbb{N^+}$ 

Nous construisons le tableau de déterminisation : 

| $E/S$ |  .  |   a  |  b  |
|:-----:|:---:|:----:|:---:|
|  $E$  |  A  | A, B |  B  |
|  $S$  |  B  |   C  |  C  |
|       |  C  |   C  |  C  |

Le tableau déterminisé donne :

| $E/S$ |  .  |  a  |  b  |
|:-----:|:---:|:---:|:---:|
|  $E$  |  A  |  AB |  B  |
|  $S$  |  B  |  C  |  C  |
|  $S$  |  AB | ABC |  BC |
|  $S$  | ABC | ABC |  BC |
|  $S$  |  BC |  C  |  C  |
|       |  C  |  C  |  C  |

<br>
<br>
<br>
<br>
<br>
<br>

$$\EX{8}$$

!!! quote ""
    ```mermaid
    graph LR
        style ENTREE height:0px;
        style ENTREE2 height:0px;
        style SORTIE  height:0px; 
        style SORTIE2  height:0px; 

        0((0))
        2((2))
        1((1))

        0 --> SORTIE[ ]
        ENTREE[ ] --> 0 
        ENTREE2[ ] --> 1
        2 --> SORTIE2[ ]



        0 --b--> 2
        0 --b--> 1 
        
        1 --a,b--> 2 
        1 --a--> 0 
        
        2 --a--> 0    
    ```


Nous construisons le tableau de déterminisation : 

| $E/S$ |  .  |   a  |   b  |
|:-----:|:---:|:----:|:----:|
| $E/S$ |  0  |   .  | 1, 2 |
|  $E$  |  1  | 0, 2 |   2  |
|  $S$  |  2  |   0  |   .  |

Le tableau déterminisé donne :

| $E/S$ |  .  |  a  |  b  |
|:-----:|:---:|:---:|:---:|
| $E/S$ |  01 |  02 |  12 |
|  $S$  |  02 |  0  |  12 |
|  $S$  |  12 |  02 |  2  |
|  $S$  |  2  |  0  | $P$ |
|  $S$  |  0  | $P$ |  12 |
|       | $P$ | $P$ | $P$ |
