
# getuseroption

<!-- tabs:start -->

#### **English**

Get the value of a setting from the **User Options** in the Scripts Settings tab(script setup) and store it in a variable, that can be used in functions and conditions.

> It's used to get the value of what the user selected in the Script Setup and use it in the Actions.


#### **Portuguese**

Obter o valor de uma configuração do **User Options** na aba Script Settings(script setup) e guardar em uma variável, que pode ser usada em funções e condições.

> É utilizado para pegar o valor que o usuário selecionou no Script Setup e usar nas Actions.

<!-- tabs:end -->



**getuseroption**(`widget name`)

- **Parameters**
  - `widget name:` name of the widget to get the **value** from.


**Return Value**

Returns the value of the widget upon success, or `-1` otherwise.

---

**Examples**

1. Get the potion selected in the *combobox* widget with `name` **potionToUse**, then check if have less than `100` and go to a label if true.

```action
$potion = getuseroption(potionToUse)
if (itemcount($potion) < 100) then gotolabel(refill)
```

Widget JSON example:

```json
{
    "name": "potionSettings",
    "text"     : "Potion Settings",
    "children" : [
        {
            "type"        : "combobox",
            "name"        : "potionToUse",
            "text"        : "Mana Potion",
            "description" : "Which mana potion you will use?",
            "filter"      : "potion",
            "value"       : "strong mana potion"
        }
    ]
}

```


2. Get the ammunition selected in the *combobox* widget with `name` **distanceWeapon** and buy `1000` units of the item, decreasing the amount the char already have.

```action
$ammunition = getuseroption(distanceWeapon)
$ammunitionInBackpack = itemcount($ammunition)
buyitemnpc($ammunition, 1000, $ammunitionInBackpack)
```

Widget JSON example:

```json
{
	"name": "paladinSettings",
	"text"     : "Paladin Settings",
	"children" : [
		{
			"type"        : "combobox",
			"name"        : "distanceWeapon",
			"text"        : "Distance weapon",
			"description" : "Which distance weapon you will use?",
			"filter"      : ["Ammunition", "Distance Weapons"],
			"value"       : "diamond arrow"
		}
	]
}
```