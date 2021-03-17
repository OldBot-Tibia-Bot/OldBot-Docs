
# follownpc

<!-- tabs:start -->

#### **English**

Search for the NPC's name image on the screen, the NPC must be visible in the Battle List to be found.

> The image of the NPCs are stored at `$OldBotDirectory/Data/NPCs/` folder.
>
> In case there is no image with the name of the NPC you want, you can take a screenshot, crop it on Paint and save it in this folder, and also please send the image so we can add in the OldBot's files aswell.


#### **Portuguese**

Procurar pela imagem do nome do NPC na tela, o NPC deve estar visivel no Battle List para ser localizado.

> A imagem dos NPCs estão guardadas na pasta `$DiretorioOldBot/Data/NPCs/`.
>
> Caso não haja a imagem do NPC que você quer, você pode tirar uma screenshot, recortar no Paint e salvar nessa pasta, e também por favor nos envie a imagem para que possamos adicioanr nos arquivos do OldBot também.


<!-- tabs:end -->

**follownpc**(`NPC name`)


- **Parameters**
  - `NPC name:` name of the NPC to search and follow.


**Return Value**

Returns `true` upon success, or `false` otherwise.

---

**Examples**

1. Search for the first name **Captain**, useful for following the ship NPCs.

```action
follownpc(Captain)
```

2. Search for the NPC **Eremo** and follow him.

```action
follownpc(Eremo)
```