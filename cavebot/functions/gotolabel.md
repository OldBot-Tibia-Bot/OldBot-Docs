
# gotolabel


<!-- tabs:start -->

#### **English**

Go to the waypoint with the label name, if it's a number, go to the waypoint with that number in the current Tab. If the label name is a `Tab` name, go to the first waypoint of that Tab.
Hello!

#### **Portuguese**

Ir para o waypoint com o nome do label, se for um numero, irá para o waypoint com aquele número na Aba atual. Se o nome do label é o nome de uma `Aba`, irá para o primeiro waypoint dessa Aba.

<!-- tabs:end -->

```action
gotolabel(param)
```

- **Parameters**
  - `param:` waypoint number, waypoint label or tab name


**Return Value**

Returns `true` upon success, or `false` otherwise.

---

**Examples:**

#1: Go to the waypoint with **label** "BuySupply" if has less than `50 mana potions`.
```action
if (itemcount(mana potion) < 50) then gotolabel(BuySupply)
```

#2: Go to the first waypoint of the current `Tab`.
```action
gotolabel(1)
```

#2: Go to the first waypoint of a tab named `Hunt`.
```action
gotolabel(Hunt)
```