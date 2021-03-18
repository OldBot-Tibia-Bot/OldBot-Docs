
# travel

<!-- tabs:start -->

#### **English**

The Cavebot can get a little messy when your char is at one position and gets teleported far away, by travelling by boat for example. With this function, this situation is handled by the bot by checking your current and destination position, to check if you have traveled and make this process faster.

This functions handles to follow the NPC(optional), start the conversation with him, say the destination name and then checking if you got to the destination position.

#### **Portuguese**

O Cavebot pode ficar um pouco confuso quando o seu char está em uma posição e é teleportado para longe, ao viajar de barco por exemplo. Com essa função, essa situação é tratada pelo bot checando sua posição atual e a posição de destino, para checar se você viajou e tornar esse processo mais rápido.

Essa função cuida de seguir o NPC(opcional), iniciar a conversa com ele, falar o nome do destino e depopis checar se você chegou na posição do destino.


<!-- tabs:end -->

**travel**(`location`, `NPC name*`)


- **Parameters**
  - `location:` the name of the destionation you will travel to.
  - `NPC name:` optional param; if set, will search for the NPC in the Battle List to follow it before starting sending messages;


**Return Value**

Returns `true` upon success, or `false` otherwise.

---

**Examples**

1. Try to follow any NPC whose first name is **Captain** and then travel to **Venore**.

```action
travel(Venore, Captain)
```

2. Try to follow the NPC **Captain Bluebear** and then travel to **Edron**.

```action
travel(Edron, Captain Bluebear)
```

