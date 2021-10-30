
# presskey

<!-- tabs:start -->

#### **English**

Press a keyboard hotkey.

> - Key modifiers:
>   - Shift: `+`
>   - Control: `^`
>   - Alt: `!`

!> Avoid using hotkeys with key modifiers, since they have higher chance of failing/causing keyboard input interference.

#### **Portuguese**

Pressionar uma hotkey do teclado.

> - Key modifiers:
>   - Shift: `+`
>   - Control: `^`
>   - Alt: `!`

!> Evite usar hotkeys com key modifiers, pois eles tem maior chance de falhar/causar interferencia de keyboard input.

<!-- tabs:end -->

**presskey**(`key`, `repeat*`, `delay*`)


- **Parameters**
  - `key:` name of the key, must be the **same** as in the [AutohHotkey's Key list](https://www.autohotkey.com/docs/KeyList.htm#keyboard).
  - `repeat:` optional param; times to press, default is 1.
  - `delay:` optional param; the interval delay in **miliseconds** after each key press, default is 250.


**Return Value**

Nothing.

---

**Examples**

1. Press **Down** arrow key 3 times, wait 400ms after each press.

```action
presskey(Down, 3, 400)
```

2. Press **F1** key holding `Shift` once.

```action
presskey(+F1)
```

3. Press **F1** key holding `Ctrl` once.

```action
presskey(^F1)
```

