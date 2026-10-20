# VrzzN Digital

Oráculo de RPG solo para jogar na tela. Faça uma pergunta de sim ou não, role dois dados e deixe o oráculo responder. Também reúne tabelas D66 de eventos, palavras, NPCs, ganchos de história e clima.

**Online:** https://guicaol.github.io/VrzznDigital/

## Como funciona

O oráculo usa dois dados de seis lados:

- **Dado 1 (resposta):** 1 a 3 é **não**, 4 a 6 é **sim**.
- **Dado 2 (evento):** se os dois dados mostrarem o mesmo número, acontece um evento. Nesse caso o site rola na tabela de eventos (D66).

D66 significa rolar dois d6: o primeiro é a dezena e o segundo é a unidade. Resultado 3 e 5 = 35.

## Ferramentas

| Seção | O que faz |
|---|---|
| Oráculo | Pergunta de sim ou não com dois dados, com opção de digitar os valores dos seus dados físicos |
| Eventos | Sorteia direto um dos 18 eventos, sem passar pelo sim ou não |
| Palavras | Três colunas de 36 palavras para ideias e descrições, em sorteio de 3 ou de 1 palavra |
| NPC | Sete rolagens: modificador, papel, motivação, intenção, desejo, reação inicial e humor |
| Ganchos | Um assunto e um acontecimento formam a ideia inicial de uma cena |
| Clima | 36 climas para abrir ou mudar uma cena |
| Consulta | Escolha uma tabela e digite os dois dados para ver o resultado de uma rolagem física |
| Histórico | As últimas 30 rolagens da sessão |

## Detalhes

- Os dados são sorteados com `crypto.getRandomValues`, sem viés de módulo.
- O histórico, a preferência de som e o tema (escuro ou claro) ficam no `localStorage` do navegador. Cada pessoa e cada aparelho têm o seu próprio histórico.
- O som é gerado pelo navegador com Web Audio e pode ser desligado no botão do topo.
- A animação dos dados respeita a preferência do sistema por menos movimento.
- O tema escuro ou claro segue o sistema e pode ser trocado no botão "Tema".

## Visual

A página é desenhada como o tampo de uma mesa de jogo: feltro ao fundo, trilho de madeira na navegação, uma bandeja onde os dados rolam e fichas de papel para cada ferramenta. O resultado do oráculo aparece como uma ficha com o SIM ou NÃO carimbado.

Fontes: [Young Serif](https://fonts.google.com/specimen/Young+Serif) e [Source Serif 4](https://fonts.google.com/specimen/Source+Serif+4), carregadas pelo Google Fonts.

## Rodar localmente

Não há dependências nem etapa de build. É um único arquivo.

1. Baixe o `index.html`.
2. Abra no navegador.

As fontes do Google precisam de internet. Sem conexão, a página usa as fontes serifadas do sistema.

## Publicar no GitHub Pages

1. Deixe o `index.html` na raiz do repositório.
2. Em **Settings > Pages**, escolha **Deploy from a branch**, selecione `main` e `/ (root)`.
3. O site fica disponível em `https://<usuario>.github.io/<repositorio>/`.

## Estrutura

```
index.html   página inteira: HTML, CSS e JavaScript
README.md    este arquivo
```

## Créditos

Tabelas e regras do oráculo VrzzN, adaptadas para uso na tela.
