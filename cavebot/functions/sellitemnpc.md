
# sellitemnpc

<!-- tabs:start -->

#### **English**

Sell all the amount of an item that you have in the NPC nearby, it works by saying "hi", opening the Trade window and searching for the item to sell.

#### **Portuguese**

Vende toda a quantidade de um item que você tem no NPC por perto, o funcionamento se dá falando "hi", abrindo a janela do Trade e procurando pelo item para vender.


<!-- tabs:end -->


**sellitemnpc**(`item name`)

- **Parameters**
  - `item name:` name of the item to buy.


**Return Value**

Returns `true` upon success, or `false` otherwise.

---

**Examples**

1. Sell the **empty potion flask**, it will sell all the three types of empty potions.

```action
sellitemnpc(empty potion flask)
```
