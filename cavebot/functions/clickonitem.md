
# clickonitem

<!-- tabs:start -->

#### **English**

Search for the item on screen and click on it, if the item has more than 1 sprite, it will to search for all its sprites variations of the `ItemList`. Items with more than one sprites and with animation takes more time to search.

?> The item must be visible in the backpack slots or any other slot to be found.

#### **Portuguese**

Procura pelo item na tela e clica nele, se o item tem mais de 1 sprite, irá procurar por todas as suas variações de sprites do `ItemList`. Items com mais de uma sprite e com animação levam mais tempo para procurar.

?> O item deve estar visivel no slot de backpack ou qualquer outro slot para ser localizado.

<!-- tabs:end -->

**clickonitem**(`item name`, `click`, `repeat*`, `delay*`)


- **Parameters**
  - `item name:` name of the item, the same as in the `ItemList`.
  - `click:` **left** or **right**.
  - `repeat:` optional param; times to click, default is 1.
  - `delay:` optional param; the interval delay in **miliseconds** after each click, default is 500.


**Return Value**

Returns `true` upon success, or `false` otherwise.

---

**Examples**

1. Right click on **brown mushroom** `3` times, wait `1000`ms after each click.

```action
clickonitem(brown mushroom, Right, 3, 1000)
```
