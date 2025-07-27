# Substituições de Arquivos e Adições

## Substituições de Arquivos

O principal recurso que o Polymod permite é substituir recursos. Isso é feito adicionando esses arquivos à sua pasta de mods, no mesmo local onde eles seriam colocados.

Por exemplo, pode substituir os sprites da GirlFriend (eu não vou traduzir os nomes) colocando os seus novos sprites no mesmo local em que eles estão na pasta `assets`, que seria `shared/images/characters/GF_assets.png`.

Em outras palavras, estruture o seu mod da seguinte forma:

```
-assets
-manifest
-plugins
-mods
 |-myMod
   |-shared
     |-images
       |-characters
         |-GF_assets.png
         |-GF_assets.xml
   |-_polymod_meta.json
-Funkin.exe
```

Quando o jogo vai carregar os sprites de um personagem, ele faz uma solicitação interna para recuperar o arquivo `assets/shared/images/characters/GF_assets.png` para usar na textura (e o `XML` correspondente para dividir a imagem em quadros individuais). Quando isso acontece, o Polymod intercepta essa solicitação e verifica se existe um arquivo com esse nome entre os mods carregados e, se existir, ele será usado.

## Adições de Arquivos

O Polymod também permite adicionar novos arquivos ao jogo. Isto é importante, pois tentar colocar novos arquivos no diretório «assets» não funciona, o jogo não reconhecerá esses arquivos.

O jogo ainda precisa ser instruído a carregar esses recursos para que eles sejam usados, mas há muitas funções que carregam todos os arquivos em uma determinada pasta (como o Registo de Músicas, o Registo de Personagens, o Registo de Palcos, etc.). Veremos isso com mais detalhes posteriormente.