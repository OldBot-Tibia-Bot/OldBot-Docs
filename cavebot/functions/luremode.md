
# luremode

<!-- tabs:start -->

#### **English**

The lure mode changes the way the Targeting system behaviours, it will count the creatures in the Battle List constantly while walking(Cavebot running), and will stop walking to attack the creatures only if the amount is higher or equal than the amount that has been set as parameter in this function.

!> If you get trapped while walking with lure mode enabled, it will ignore the lure mode to attack and kill the creatures, and then enabled it again.

#### **Portuguese**

O lure mode altera o funcionamento do sistema do Targeting, irá contar as criaturas no Battle List constantemente enquanto caminha(Cavebot rodando), e irá parar de caminhar para atacar as criaturas somente se a quantidade for maior ou igual a quantidade que foi setada como parâmetro nessa função.

!> Se você ficar trapado enquanto caminhando com o lure mode ativo, irá ignorar o lure mode para atacar e matar as criaturas, e posteriormente habilitar novamente.



<!-- tabs:end -->

**luremode**(`amount of creatures`)


- **Parameters**
  - `amount of creatures:` the number of creatures in the Battle List to start attacking.


**Return Value**

Nothing.


?> You can add a Action waypoint with the `luremode` function **only once** in the script.

You don't need to add many waypoints with `luremode` in different parts of the script, once it runs the function, the lure mode will continue to be enabled until it reaches a `luremodestop()` function.

---

**Examples**

1. Sets the lure mode to only stop to attack with 3 or more creatures in the Battle List.

```action
luremode(3)
```

2. Get the selected user option value with name `amountCreaturesLure` and use it as the parameter for the lure mode function.

```action
$creaturesLure = getuseroption(amountCreaturesLure)
luremode($creaturesLure)
```

