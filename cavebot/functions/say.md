
# say

<!-- tabs:start -->

#### **English**

Write and send a message in the **current** chat. It turns to `Chat On` to send and then to `Chat Off`.

?> To start a conversation with a NPC, avoid using this function to say "hi", use the `npchi()` function instead, which it is meant for this purpose.

?> If you want to make sure you will send the message in the "Local Chat", you can use the action `presskey(!d)` *(Alt+D)* to change the chat.<br><br>For additional info of chat commands, check this [TibiaWiki's link] (https://tibia.fandom.com/es/wiki/Chat_Commands).

#### **Portuguese**

Escrever e enviar uma mensagem no chat **atual**. Será alterado para `Chat On` para enviar e depois para `Chat Off`.

?> Para iniciar uma conversa com um NPC, evite usar essa função para falar "hi", use a `npchi()` ao invés, que é feita para esse propósito.

?> Se você quer ter certeza que a mensagem será enviada no "Local Chat", você pode usar a action `presskey(!d)` *(Alt+D)* para mudar o chat.<br><br>Para informações adicionais de comandos de chat, cheque esse [link do TibiaWiki] [TibiaWiki's link] (https://tibia.fandom.com/es/wiki/Chat_Commands).


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
