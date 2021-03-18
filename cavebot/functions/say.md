
# say

<!-- tabs:start -->

#### **English**

Write and send a message in the current chat. It turns to "Chat On" to send and then to "Chat Off".

?> If you want to start a conversation with a NPC, avoid using this function to say "hi", use the `npchi()` function instead, which it is meant for this purpose.

#### **Portuguese**

Escrever e enviar uma mensagem no chat atual. Será alterado para "Chat On" para enviar e depois para "Chat Off".

?> Se você quer iniciar uma conversa com um NPC, evite usar essa função para falar "hi", use a `npchi()` ao invés, que é feita para esse propósito.


<!-- tabs:end -->

**say**(`message`)


- **Parameters**
  - `message:` message to send.


**Return Value**

Returns `true` upon success, or `false` otherwise.

---

**Examples**

1. Say message **oldbot rocks** on the current chat.

```action
say(oldbot rocks)
```
