# Ordem Paranormal para o ATO20

Plugin que põe Ordem Paranormal no ATO20, em duas partes. É só o
`manifest.json`, sem código.

- **O sistema:** ao criar a campanha (ou depois, em Configuração da campanha,
  Sistema), ela nasce com AGI, FOR, INT, PRE e VIG, os medidores PV, PE e SAN,
  a ficha de agente nos detalhes (Identidade, Combate, as 28 perícias,
  Habilidades e rituais, Ataques e Descrição) e 16 condições do jogo.
- **A ficha em PDF:** na lista de Personagens, **Importar ficha em PDF** cria
  o personagem a partir da ficha de agente editável, com o PDF anexado como a
  ficha dele. Com o sistema aplicado, tudo cai nos detalhes do molde.

## O sistema

| | Começa com |
| --- | --- |
| Atributos | AGI, FOR, INT, PRE e VIG, em 1 |
| Medidores | PV 20, PE 2 e SAN 12 (a base de Combatente) |
| Identidade | jogador, origem, classe (Combatente, Especialista, Ocultista), trilha, NEX 5, PE por rodada 1, deslocamento 9m, patente (Recruta a Agente de elite), pontos de prestígio |
| Combate | defesa 10, proteção, resistências, DT de rituais |
| Perícias | as 28, em 0 |
| Listas | Habilidades e rituais, Ataques, e Descrição (aparência, personalidade, histórico, objetivo) |
| Condições | Machucado, Morrendo, Sangrando, Perturbado, Enlouquecendo, Abalado, Apavorado, Atordoado, Desprevenido, Agarrado, Caído, Fatigado, Envenenado, Cego, Paralisado e Inconsciente |

Aplicar junta ao que a campanha já tem: o que tiver o mesmo nome fica como o
mestre deixou.

## A ficha

O plugin lê a ficha de agente **editável** feita no PDFescape, a que tem os
campos `untitled1` a `untitled340`. A impressa, a digitalizada e a que não tem
formulário continuam entrando como anexo.

O PDF da ficha não vem no plugin: ela é da Jambô Editora.

## O que vira o quê

| Na ficha | No personagem |
| --- | --- |
| Personagem | o nome |
| AGI, FOR, INT, PRE, VIG | atributos |
| PV, PE e SAN, atuais e máximos | medidores PV, PE e SAN |
| Jogador, origem, classe, NEX, PE por rodada, deslocamento, patente, prestígio | detalhes em Identidade |
| Defesa, proteção, resistências, DT de rituais | detalhes em Combate |
| As 28 perícias, pelo bônus | detalhes em Perícias |
| Aparência, personalidade, histórico, objetivo | detalhes em Descrição, cada um com as cinco linhas juntas |
| Ataques (teste, dano, crítico/alcance) | uma linha por ataque em Ataques |
| Habilidades & rituais (custo, descritivo) | uma linha por habilidade em Habilidades e rituais |

O inventário fica de fora por enquanto: ele segue no PDF anexado.

## Instalar

Pede o ATO20 com a API de plugins 10.

1. Clone o repositório (ou baixe o zip dele):

   ```
   git clone https://github.com/ato20-org/ato20.ordem-paranormal.plugin
   ```

2. No ATO20, Configurações, Plugins, **Importar plugin**, e escolha a pasta.

Funciona ao lado do Segredo na Floresta: o medidor que a campanha já tem com
o mesmo nome (PV, PE, SAN) continua com o estilo que o mestre escolheu, as
barras de pincel por exemplo, e a ficha só diz quanto.
