
# takeitemfromstash

<!-- tabs:start -->

#### **English**

Walk to a free depot, open the Supply Stash and take the specified amount of the item.

?> Only premium accounts can use the Stash in Tibia.

!> Currently items with more than `9999` units in the Stash **will fail** to take, since the amount change from thousand to **10**`k`+.

#### **Portuguese**

Caminha até um depot livre, abre o Supply Stash e pega a quantidade especificada do item.

?> Somente premium accounts podem usar o Stash no Tibia.

!> Atualmente itens com mais de `9999` unidades no Stash **irão falhar** para pegar, já que a quantidade é alterada de milhar para **10**`k`+.


<!-- tabs:end -->

**takeitemfromstash**(`item name`, `amount to buy`, `amount to decrease*`)

- **Parameters**
  - `item name:` name of the item, the same as in the `ItemList`.
  - `amount to buy:` self explained.
  - `amount to decrease:` optional param; the amount to decrease from the buy amount, it's what used to decrease how many of the item your char already have before buying more.

> The parameters are the same as the [`buyitemnpc`](cavebot/functions/buyitemnpc.md) function.

**Return Value**

Returns `true` upon success, or `false` otherwise.

---

**Examples**

1. Take `100` **mana potion** from the Stash.

```action
takeitemfromstash(mana potion, 100)
```

2. Take `500` **assassin star** from the Stash, decreasing how many you already have.

```action
$amountAssassinStar = itemcount(assassin star)
takeitemfromstash(assassin star, 500, $amountAssassinStar)
```

