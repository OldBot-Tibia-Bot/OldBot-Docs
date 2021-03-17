
# deposititems

<!-- tabs:start -->

#### **English**

Deposit the items set up on `Looting > DepositList`. It walks to a free depot SQM, opens the depot locker and deposit the items.

If the **stash backpack** is specified as the parameter, it'll move the backpack to the Stash, depositing every stackable item in it at once.

?> Only premium accounts can use the Stash.

#### **Portuguese**

Depositar os itens configurados em `Looting > DepositList`. Irá caminhar até um SQM livre de depot, abrir o depot locker e depositar os itens.

Se a **stash backpack** for especificada no parâmetro, irá mover a backpack para a Stash, depositando todos os itens stackáveis de uma vez só.

?> Somente premium accounts podem usar o Stash.

<!-- tabs:end -->

**deposititems**(`stash backpack*`)


- **Parameters**
  - `stash backpack:` optional param; name of a backpack to move to the Stash


**Return Value**

Returns `true` upon success, or `false` otherwise.


---

**Examples**

1. Deposit items and also deposit the golden backpack in the Stash.

```action
deposititems(golden backpack)
```

2. If `$depositStashBP` variable is a backpack, it will deposit the entire backpack in the Stash. You can use `takeitemfromstash()` function to take items(such as potions).

```action
$depositStashBP = getuseroption(depositStashBackpack)
deposititems($depositStashBP)
```

