
# droptrash

<!-- tabs:start -->

#### **English**

Search for all the items of the list in `Looting > TrashList` and drop them in the character's position.

#### **Portuguese**

Procura por todos os items da lista em `Looting > TrashList` e os dropa na posição do char.

<!-- tabs:end -->

**droptrash**()

No Parameters

**Return Value**

Nothing.

---

**Examples**

1. Drop trash if **cap** is lower than 100.

```action
if (capacity() < 100) then droptrash()
```
