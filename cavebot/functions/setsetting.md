
# setsetting

<!-- tabs:start -->

#### **English**

Set a value to a setting in the script JSON. This is a very useful action that opens many possibilites to change settings and start/stop functions while the Cavebot is running.

#### **Portuguese**

Setar o valor de uma configuração no JSON do script. Essa é uma action muito útil que abre muitas possibilidades para alterar configurações e parar/iniciar funções enquanto o Cavebot está rodando.

<!-- tabs:end -->


**setsetting**(`setting path`)

- **Parameters**
  - `setting path:` the path of the setting, following the structure of the script JSON, separated by slash `/`.


**Return Value**

Returns `true` upon success, or `false` otherwise.

?> To know what is the setting path of the option you want to check, you must open the script JSON file in any text editor(recommended is [Sublime Text](https://www.sublimetext.com/)) and follow its structure.


For example, if I want to enable the **player on screen** alert, I open the script JSON file and see this:

![](../../_media/cavebot/functions/getsetting_example.png)

`alerts` is the main setting, it has other child settings, one of them is `playerOnScreen`, that also has child settings, we want to check the `enabled` setting.

So the path will be `alerts/playerOnScreen/enabled`, and the `setsetting` function:
```action
setsetting(alerts/playerOnScreen/enabled, 1)
```

---

**Examples**

1. Disable Looting.

```action
setsetting(looting/settings/lootingEnabled, 0)
```

2. Enable the Auto Reconnect.

```action
setsetting(reconnect/autoReconnect, 1)
```

3. Stop the Ring Refill function.

```action
setsetting(itemRefill/ringRefillEnabled, 0)
```

4. Disable the `Equip Ring` function for the creature **swamp troll** in the Targeting settings, by changing the `ringHotkey` value, setting it empty.

```action
setsetting(targeting/targetList/swamp troll/ringHotkey, )

```

5. Disable the internal disconnected check of the Cavebot System, this allows the waypoints to run even if the character is disconnected(to interact with the client for example).

```action
setsetting(cavebotSystem/checkDisconnected, 0)
```

6. Change the **Cavebot Functioning Mode** when it is running(requires to restart the Cavebot), this is useful to get out of the `Coordinates` functioning mode in custom map areas where it may not be working correctly.

```action
setsetting(scriptSettings/cavebotFunctioningMode, Markers)
reloadcavebot()

# ...waypoints...

setsetting(scriptSettings/cavebotFunctioningMode, Coordinates)
reloadcavebot()

# ...waypoints...
```

7. Stop the Persistent of ID `1`.

```action
setsetting(persistent/1/enabled, 0)
```

8. Start the Persistent of ID `3`.

```action
setsetting(persistent/3/enabled, 1)
```

9. Change the **Default menu click method** setting to `0`.

```action
setsetting(scriptSettings/defaultMenuClickMethod, 0)
```

10. Change the default limit of how many times the bot scrolls down the Trade List when buying/selling items to NPC. The default is `60`. It may be needed to increase when buying items with the npc "Rock in a hard place".

```action
setsetting(cavebotSystem/scrollDownLimit, 120)
```

11. Disable and enable the Alert `Image is found 1`, this will cause the "label" trigger from **Go to label** option to reset and be able to trigger again.

```action
setsetting(alerts/Image is found 1/enabled, 0)
wait(1000)
setsetting(alerts/Image is found 1/enabled, 1)
`````

12. Disable and enable the Persistent of ID `1`, this will cause the "label" trigger from **Go to label if itemcount** option to reset and be able to trigger again.

```action
setsetting(persistent/1/enabled, 0)
wait(1000)
setsetting(persistent/1/enabled, 1)
```

13. Change the Persistent "Go to label if itemcount" parameters from Cavebot, useful to set the values with information from the Script Setup.
```
# ID of persistent "Go to label if itemcount"
$persistentId = 14

# Item to count
$item = mana potion

# Go to label if count is lower than:
$countToLeave = 99

# unlikely to change
$keyItemName = 2
$keyCountValue = 4

setsetting(persistent/$persistentId/userValue/$keyItemName/item, $item)
setsetting(persistent/$persistentId/userValue/$keyCountValue/value, $countToLeave)
```