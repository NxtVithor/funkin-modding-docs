# Ordem de Carregamento de Mods

Pode estar se questionando o que acontece no caso de vários mods fornecerem um determinado arquivo.

A resposta é simples: a ordem dos mods é importante. Se tiver dois mods instalados que substituem um determinado recurso, o mod que for carregado por último terá precedência sobre os mods que forem carregados anteriormente, semelhante ao sistema de pacotes de recursos do Minecraft. Isso é avaliado por arquivos, portanto, se o Mod A substituir o Pico e o GF e o Mod B substituir apenas o GF, e o Mod B for carregado depois do Mod A, verá o Pico do Mod A e a Girlfriend do Mod B.

Na versão atual do Friday Night Funkin', não há meios acessíveis de alterar a ordem de carregamento dos mods. Os mods serão carregados em ordem alfabética por predefinição, com as dependências a serem carregadas primeiro.