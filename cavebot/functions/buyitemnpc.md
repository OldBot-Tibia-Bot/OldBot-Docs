
# buyitemnpc

<!-- tabs:start -->

#### **English**

Buy a specified amount of an item in the NPC nearby, it works by saying "hi", opening the Trade window and searching for the item to buy.

#### **Portuguese**

Compra uma quantidade especificada de um item no NPC por perto, o funcionamento se dá falando "hi", abrindo a janela do Trade e procurando pelo item para comprar.


<!-- tabs:end -->


**buyitemnpc**(`item name`, `amount to buy`, `amount to decrease*`)

- **Parameters**
  - `item name:` name of the item to buy.
  - `amount to buy:` self explained.
  - `amount to decrease:` optional param; the amount to decrease from the buy amount, it's what used to decrease how many of the item your char already have before buying more.


**Return Value**

Returns `true` upon success, or `false` otherwise.

---

**Examples**

1. Buy `100` **strong mana potion**

```action
buyitemnpc(strong mana potion, 100)
```

2. Buy `100` **mana potion**, but count how many you have to decrease in the amount before buying.

```action
$amountManaPotion = itemcount(mana potion)
buyitemnpc(mana potion, 100, $amountManaPotion)

```

