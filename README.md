# Copiloto de Vendas para Loja de Pecas e Computadores

Este projeto apresenta um copiloto de vendas com IA para apoiar atendentes de uma loja especializada em pecas, computadores montados, upgrades e servicos tecnicos. A proposta e ajudar o vendedor a responder mais rapido, recomendar combinacoes coerentes e conduzir o atendimento com mais seguranca.

## Tema escolhido

O copiloto foi personalizado para uma loja de pecas e computadores chamada **ByteCerto Computadores**.

- Area de atuacao: venda de pecas, computadores montados, notebooks e servicos de upgrade
- Publico-alvo: gamers, clientes de home office, estudantes, profissionais de criacao e pequenos negocios

## Problema que o copiloto ajuda a resolver

No atendimento de informatica, o vendedor precisa entender o perfil do cliente, verificar compatibilidade, responder duvidas tecnicas, contornar objecoes de preco e ainda manter a conversa organizada. O copiloto ajuda a:

- sugerir produtos e servicos de acordo com uso e orcamento;
- responder duvidas comuns com linguagem simples;
- apoiar o tratamento de objecoes sem pressionar o cliente;
- sugerir a proxima mensagem ou follow-up ideal.

## Abordagem usada

Foi usada uma abordagem de **copiloto + chatbot guiado por prompt**:

- `prompts/prompt-principal.md` define o comportamento do assistente;
- `knowledge/` concentra as informacoes do negocio;
- `AGENTS.md` descreve o papel do agente de forma objetiva.

Essa estrutura permite usar o material em ferramentas como ChatGPT, Codex ou outras interfaces de IA com base em prompt e conhecimento de negocio.

## Informacoes utilizadas

A base de conhecimento foi organizada em tres frentes:

- `knowledge/produtos.md`: linhas de produtos, servicos, perfis de uso e observacoes de compatibilidade;
- `knowledge/perguntas-frequentes.md`: respostas para duvidas recorrentes no atendimento;
- `knowledge/objecoes.md`: objecoes comuns de vendas e formas recomendadas de responder.

## Estrutura do projeto

```text
chatbot-vendas-desafio/
  README.md
  AGENTS.md
  prompts/
    prompt-principal.md
  knowledge/
    produtos.md
    perguntas-frequentes.md
    objecoes.md
```

## Exemplo de uso

### Pedido do vendedor

> Cliente quer um computador para jogos competitivos e estudos. Orcamento maximo de R$ 6.500. Perguntou se vale mais pegar um PC pronto ou montar por partes.

### Resposta esperada do copiloto

> Para esse perfil, o melhor caminho e um PC gamer intermediario com foco em bom desempenho em Full HD e possibilidade de upgrade. A opcao mais aderente e o **PC Gamer Start**, com Ryzen 5, 16 GB de RAM, SSD NVMe de 1 TB e RTX 4060.
>
> Argumentos principais:
> - atende jogos competitivos com folga em Full HD;
> - tambem serve bem para estudos e multitarefa;
> - permite upgrade futuro de memoria e armazenamento.
>
> Resposta pronta para o cliente:
> "Para o seu uso, eu indicaria um PC montado com configuracao equilibrada. Assim voce leva um conjunto ja testado, com garantia do sistema inteiro e desempenho muito bom para jogos competitivos e estudos, sem precisar se preocupar com compatibilidade entre as pecas."
>
> Proxima mensagem sugerida:
> "Se quiser, eu posso te passar duas opcoes dentro do seu orcamento: uma mais focada em custo-beneficio e outra pensando em mais tempo de vida util."

## Possiveis melhorias futuras

- integrar estoque e precos reais;
- buscar historico do cliente em CRM ou WhatsApp;
- gerar comparativos automaticos entre configuracoes;
- montar orcamentos com parcelas e prazo de entrega;
- registrar as objecoes mais frequentes para treinar o time comercial.

## Como usar

1. Abra o `prompts/prompt-principal.md`.
2. Use o prompt junto com os arquivos da pasta `knowledge/`.
3. Envie para a IA o contexto do atendimento, incluindo necessidade, orcamento e duvidas do cliente.
4. Use a resposta como apoio ao vendedor, ajustando o tom para a conversa real.
