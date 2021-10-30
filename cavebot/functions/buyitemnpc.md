
# buyitemnpc

<!-- tabs:start -->

#### **English**

Buy the specified amount of an item in the NPC nearby, it works by saying "hi", opening the Trade window and searching for the item to buy.

> When buying **potions** or **runes**, it will filter the Trade window list before buying.

!> By default it buys the items very fast, but in some OT servers there is an additional delay to prevent buying items too fast, in this case you should adjust the internal Cavebot delay using this action before buying:<br>`setsetting(cavebotSystem/buyItemDelay, 1200)`


#### **Portuguese**

Compra a quantidade especificada de um item no NPC por perto, o funcionamento se dá falando "hi", abrindo a janela do Trade e procurando pelo item para comprar.

> Ao comprar **potions** ou **runes**, irá filtrar a lista do Trade window antes de comprar.

!> Por padrão o bot compra os itens muito rápido, mas em alguns OT serves há um delay adicional para previnir a compra tão rápida, nesse caso você deve ajustar o delay interno do Cavebot antes da compra usando essa action:<br>`setsetting(cavebotSystem/buyItemDelay, 1200)`

<!-- tabs:end -->


**buyitemnpc**(`item name`, `amount to buy`, `amount to decrease*`)

- **Parameters**
  - `item name:` name of the item, the same as in the `ItemList`.
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

