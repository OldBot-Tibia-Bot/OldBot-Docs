
# itemcount

<!-- tabs:start -->

#### **English**

Count the quantity of the item you have.

!> On `Tibia 11/12+`, the item must be visible in the **Action Bar** for it to work. In `other` client versions which the function is compatible, it will count all the items visible on the screen.

#### **Portuguese**

Conta a quantidade do item que você tem.

!> No `Tibia 11/12+`, o item deve estar visível na **Action bar** para que funcione. Em clientes de `outras` versões em que a função é compatível, irá contar todos os itens visíveis na tela.

<!-- tabs:end -->

**itemcount**(`item name`)


- **Parameters**
  - `item name:` name of the item, the same as in the `ItemList`.


**Return Value**

Returns the item `quantity` upon success, or `0` otherwise.

---

**Examples**

1. Count how many **mana potion** you have and go to a label named **LeaveHunt** if have less than `50`.

```action
if (itemcount(mana potion) < 50) then gotolabel(LeaveHunt)
```
