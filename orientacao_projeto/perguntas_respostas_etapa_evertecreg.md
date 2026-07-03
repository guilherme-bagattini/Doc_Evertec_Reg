# Perguntas e respostas da etapa do EvertecReg

Este registro consolida as respostas recebidas sobre o fluxo inicial de curadoria e monitoramento.

## Leitura geral

As respostas mostram um desenho de produto mais consistente do que parecia no começo:

- o fluxo inicial e mais seguro segue o caminho de gravar e depois aprovar;
- o acesso sera restrito a poucos colaboradores da Evertec nesta etapa;
- o dashboard e a visao de notificacoes ficam como evolucao posterior;
- o status de erro deve ser generico na interface e detalhado nos logs;
- a IA vai usar duas linhas de contexto: negocio do cliente e documentacao dos produtos de software.

## Perguntas e respostas

| # | Pergunta | Resposta recebida | Leitura pratica |
| --- | --- | --- | --- |
| 1 | Aprovou errado tem como voltar? | Nao previnem voltar atras; preferem confirmacao em duas etapas: gravar e depois aprovar | O fluxo deve ser conservador e nao depender de rollback humano na interface |
| 2 | Lista de quem pode aprovar? | Nao previram segregacao de permissao nesta etapa | O MVP pode assumir acesso restrito, sem matriz complexa de perfis |
| 3 | Tem versionamento das publicacoes? | Nao previram versionamento agora | Se isso for necessario, deve virar decisao explicita de escopo |
| 4 | Tem alerta para novos itens? | Ainda nao; dashboard fica para depois do MVP | A notificacao operacional e uma evolucao de produto |
| 5 | O que seria o status erro? | Deve ser generico na tela e detalhado nos logs | Faz sentido separar resumo operacional de diagnostico tecnico |
| 6 | A tabela é editavel? | Cada conteudo dela | A interacao deve ser por item, nao por edicao massiva de grade |
| 7 | Exigir justificativa no final de cada ação? | Concordam com incluir justificativa | Boa direcao para rastreabilidade e auditoria |
| 8 | Botao aprovar confirma definitivamente? | Sim, e uma confirmacao do que ja foi decidido ao clicar em gravar | O aprovar valida a decisao previamente registrada |
| 9 | Você definiu como deve ser o BD? | Nao; a modelagem ficou com o time de dados | Esse ponto precisa acompanhamento separado |
| 10 | Ideia de escala do produto? | Entenderam como venda; talvez valha call | O tema precisa ser esclarecido antes de consolidar a visao de crescimento |
| 11 | IA vai aprender? | Nao no MVP; talvez em incremento futuro | Por ora a IA nao deve ser tratada como modelo adaptativo em producao |
| 12 | Relevancia por tema, como BACEN? | Sim, para a etapa seguinte, quando gerar cards em KANBAN | A IA deve classificar relevancia com base em documentacao de negocio e de software |

## Pontos que ficaram mais claros

- O primeiro fluxo e restrito a area e BD da Evertec.
- A IA no dominio seguinte vai classificar relevancia para cards em KANBAN.
- O contexto de classificacao combina documentacao do negocio do cliente e documentacao dos produtos de software do cliente.
- O modelo de erro deve facilitar operacao sem expor ruido tecnico na tela.

## Pendencias que merecem acompanhamento

- detalhar se e necessario algum tipo de permissao adicional no futuro;
- alinhar se a ausencia de versionamento e definitiva;
- confirmar o papel do BD e o artefato de modelagem;
- definir a leitura de escala do produto;
- validar a estrategia de dashboard e alertas para o pos-MVP.