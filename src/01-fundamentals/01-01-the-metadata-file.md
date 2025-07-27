# O Arquivo Metadata

Para começar, crie uma nova pasta dentro da pasta `mods`. É aqui que os recursos e scripts do seu mod ficarão armazenados. Em seguida, crie um novo documento de texto e altere o nome para `_polymod_meta.json`. Certifique-se de que não o nomeou acidentalmente como `_polymod_meta.json.txt`!*

`Notas do Tradutor:no seu explorador de arquivos aperte no botão superior "Exibir", e aperte na caixa selecionada como "Extensões de Nomes de Arquivos `


Dentro deste arquivo de texto, colocaremos as informações de que o jogo precisa para aprender sobre a sua modificação. Recomendo fazer isso com um programa como o [Visual Studio Code](https://code.visualstudio.com/), que irá corrigi-lo se, acidentalmente, colocar uma vírgula ou algo do género no lugar errado.

```json
{
  "title": "Intro Mod",
  "description": "Um mod introdutório.",
  "contributors": [
    {
      "name": "EliteMasterEric"
    }
  ],
  "dependencies": {
    "modA": "1.0.0"
  },
  "optionalDependencies": {
    "modB": "1.3.2"
  },
  "api_version": "0.6.3",
  "mod_version": "1.0.0",
  "license": "Apache-2.0"
}
```

O arquivo `_polymod_meta.json` tem os seguintes campos:

- `title`: Um nome legível para o mod.
- `description`: Uma descrição legível para o mod.
- `contributors`: Uma lista de Contribuidores do mod.
- `homepage`: Uma URL onde os usuarios podem saber mais sobre o seu mod.
- `dependencies`: Um mapa de IDs de mods que são dependências obrigatórias, juntamente com os seus números de versão.
  - Estes são os mods que também devem ser carregados para que este mod seja carregado.
  - Se o mod não estiver incluído, ele falhará.
  - A lista de mods será reordenada de forma que as dependências sejam carregadas primeiro.
- `optionalDependencies`: Um mapa de IDs de mods que são dependências opcionais, juntamente com os seus números de versão.
  - Estes mods não precisam necessariamente de ser instalados para que este mod seja carregado, mas ainda assim forçarão a reordenação da lista de mods para que as dependências sejam carregadas antes deste mod.
- `api_version`: Um número de versão usado para determinar se os mods são compatíveis com a sua cópia do Funkin'. Altere isso para o número da versão do Friday Night Funkin' que você deseja suportar, de preferência a mais recente (`0.6.3` no momento da redação*).
- `mod_version`: Um número de versão específico para o seu mod. Escolha qualquer versão ou deixe como `1.0.0`.
- `license`: A licença sob a qual o seu mod é distribuído. [Escolha uma aqui](https://opensource.org/licenses) ou deixe como `Apache-2.0`.

`Notas do Tradutor: Texto original de Eric foi feito na epoca que Friday Night Funkin era na versão 0.6.3`

Um colaborador tem os seguintes campos:

- `name`: O nome do colaborador.
- `role`: *(opcional)* A função desempenhada pelo colaborador, por exemplo, «Artista» ou «Programador»
- `e-mail`: *(opcional)* Um e-mail de contacto
- `url`: *(opcional)* Um URL da página inicial

Muitos destes campos destinam-se a ser utilizados no futuro por um Menu de Escolha de Mods, que permitirá aos Jogadores organizar os seus mods.