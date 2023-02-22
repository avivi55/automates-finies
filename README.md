# finite-automata-exercises
my school exercises for my finite automata class

---

## TD1

### 1

::: mermaid
graph LR
    START[ ] --> C((C)) --> STOP[ ]
    C --m--> M((M)) --> STOP2[ ]
    M --d--> D((D))
    M --v--> V((V))

    style STOP2 height:0px;

    style START height:0px;
    style STOP  height:0px;
    
:::
