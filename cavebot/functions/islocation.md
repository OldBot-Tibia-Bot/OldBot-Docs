
# islocation

<!-- tabs:start -->

#### **English**

Checks if the character's current position is at the waypoint coordinate, considering it's **range**.

> This is a very useful function to use in your scripts, to check if your char is at the right location before doing something.

#### **Portuguese**

Checa se a posição atual do char está na coordenada do waypoint, considerando seu **range**.

> Essa é uma função muito útil para ser usada nos seus scripts, para checar se o seu char está no lugar correto antes de fazer algo.


<!-- tabs:end -->

**islocation**()


No Parameters


**Return Value**

Returns `true` if it is at the coordinate, or `false` otherwise.

---

**Examples**

1. If the char is not at waypoint coordinate, go to a label named **xxx**.

```action
if (islocation() = false) then gotolabel(xxx)
```
