
# variable

<!-- tabs:start -->

#### **English**

Create and set value to script variables while the Cavebot is running, besides setting a value, it's possible to increment/decrement the current value, as shown in the examples.

<!-- Currently is not possible to do math calculations when setting value to a variable, but it is possible to increment/decrement as in the examples below. -->

> The script variables created with this function are accessed using the [`getsetting()`](cavebot/functions/getsetting.md) function, see examples below.
> <br>You can use the `variableshowall()` function to show in the log all the created variables of the script and their values.

#### **Portuguese**

Criar e setar valores a variaveis do script enquanto o Cavebot está rodando, além de poder setar um valor, é possível incrementar/decrementar o valor atual, como mostrado nos exemplos.

> As variáveis do script criadas com essa função são acessadas usando a função [`getsetting()`](cavebot/functions/getsetting.md), veja os exemplos abaixo.
> <br>Você pode usar a função `variableshowall()` para mostrar no log todas as variáveis do script criadas e seus valores.

<!-- tabs:end -->

**variable**(`name`, `value`)


- **Parameters**
  - `name:` name of the variable to be created/set value.
  - `value:` value to set to the variable, only strings/alphanumeric characters.


**Return Value**

Returns `true` upon success, or `false` otherwise.

---

**Examples**

1. Create a script variable named **myVariableName** and set it's value to `1`.

```action
variable(myVariableName, 1)
```

2. Create a script variable named **messageText** and set a `text` as its value, then get the variable value using [`getsetting()`](cavebot/functions/getsetting.md) and store in the `$textVar`, lastly show the variable value using the `messagebox()` function.

```action
variable(messageText, this is a text value for the variable)

$textVar = getsetting(scriptVariables/messageText)

messagebox($textVar)
```

3. Increment the value of the variable named **triesDeposit**.

```action
variable(triesDeposit, ++)
```

3. Decrement the value of the variable named **triesDeposit**.

```action
variable(triesDeposit, --)
```