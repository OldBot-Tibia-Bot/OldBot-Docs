
# setsetting

<!-- tabs:start -->

#### **English**

Set a value to a setting in the script JSON.

#### **Portuguese**

Setar o valor de uma configuração no JSON do script.

<!-- tabs:end -->


**setsetting**(`setting path`)

- **Parameters**
  - `setting path:` the path of the setting, following the structure of the script JSON, separated by slash `/`.


**Return Value**

Returns `true` upon success, or `false` otherwise.

?> To know what is the setting path of the option you want to check, you must open the script JSON file in any text editor(I recommend [Sublime Text](https://www.sublimetext.com/)) and follow its structure.


For example, if I want to enable the **player on screen** alert, I open the script JSON file and see this:

![](../../_media/cavebot/functions/getsetting_example.png)

`alerts` is the main setting, it has other child settings, one of them is `playerOnScreen`, that also has child settings, we want to check the `enabled` setting.

So the path will be `alerts/playerOnScreen/enabled`, and the setsetting function:
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
setsetting(itemRefill/ringRefill, 0)
```

4. Disable the `Equip Ring` function for the creature **swamp troll** in the Targeting settings, by changing the `ringHotkey` value, setting it to null(empty).

```action
setsetting(targeting/targetList/swamp troll/ringHotkey, )

```

5. disable the internal disconnected check of the Cavebot System, this allows the waypoints to run even if the character is disconnected(to interact with the client for example)..

```action
setsetting(cavebotSystem/checkDisconnected, 0)
```

