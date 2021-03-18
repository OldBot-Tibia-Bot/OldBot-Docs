
# itemcount

<!-- tabs:start -->

#### **English**

Count the quantity of the item you have.

!> The item must be visible in the **Action Bar** for it to work.

#### **Portuguese**

Conta a quantidade do item que você tem.

!> O item deve estar visível na **Action bar** para que funcione.

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
