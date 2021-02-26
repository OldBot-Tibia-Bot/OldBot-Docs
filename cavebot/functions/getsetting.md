
# getsetting

Used to get the value of a setting from the script json.

```action
gotolabel(setting path)
```


- **Parameters**
  - `setting path:` the path of the setting in the same structure as the script json;


**Return Value**

Returns the setting value upon success, or `-1` otherwise.

---

**Examples**

#1: Check if looting is enabled and enable it if disabled.

```action
$lootingEnabled = getsetting(looting/settings/lootingEnabled)
-- get looting enabled setting, which is 0 if disabled(false) or 1 if enabled(true).
if ($lootingEnabled = 0) then setsetting(looting/settings/lootingEnabled, 1)
-- enable looting if disabled.
```


#2: Get the main backpack selected on Looting > DepositList and move up to 10 `great mana potion` stacks to the backpack.

```action
$mainbp = getsetting(looting/depositSettings/backpackSettings/mainBackpack)
-- get the main backpack chosen deposit settings.
mousedragitem(great mana potion, $mainbp, 10, 500)
-- try to move great mana potion 10 times to the main backpack.
```
