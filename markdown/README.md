# Exemplos de Prompt Engineering

Este diretório organiza os exemplos por técnica de prompting.

## Índice

### Zero-Shot
- [Exemplo 1](./zero_shot/1.md)

### Few-Shot
- [Exemplo 1](./few_shot/1.md)

### Chain-of-Thought
- [Exemplo 1](./chain_of_thought/1.md)
- [Exemplo 2](./chain_of_thought/2.md)
- [Exemplo 3](./chain_of_thought/3.md)

### Tree-of-Thought
- [Exemplo 1](./tree_of_thought/1.md)
- [Exemplo 2](./tree_of_thought/2.md)
- [Exemplo 3](./tree_of_thought/3.md)

### ReAct
- [Exemplo 1](./react/1.md)
- [Exemplo 2](./react/2.md)
- [Exemplo 3](./react/3.md)

### Skeleton-of-Thought
- [Exemplo 1](./skeleton_of_thought/1.md)
- [Exemplo 2](./skeleton_of_thought/2.md)
- [Exemplo 3](./skeleton_of_thought/3.md)

### Self-Consistency
- [Exemplo 1](./self_consistency/1.md)
- [Exemplo 2](./self_consistency/2.md)
- [Exemplo 3](./self_consistency/3.md)

## Comparativo

As tabelas abaixo separam capacidade técnica de uso prático. A primeira mostra o mecanismo principal de cada abordagem. A segunda deixa explícito o que cada uma resolve melhor e o que ela não cobre sozinha.

### Capacidades por técnica

| Técnica | Usa exemplos? | Força estrutura? | Expõe raciocínio? | Explora alternativas? | Usa ferramentas? | Valida por repetição? | Melhor uso |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Zero-Shot | Não | Não | Não | Não | Não | Não | Tarefas simples e consultas diretas |
| Few-Shot | Sim | Parcial | Opcional | Não | Não | Não | Ensinar formato, estilo e padrão de saída |
| Chain-of-Thought | Opcional | Não | Sim | Não | Não | Não | Lógica sequencial, debugging e planejamento |
| Skeleton-of-Thought | Não | Sim | Opcional | Não | Não | Não | Respostas longas, documentação e tópicos fixos |
| Tree-of-Thought | Não | Parcial | Sim | Sim | Não | Não | Comparar hipóteses, estratégias e caminhos |
| ReAct | Não | Sim, no ciclo Thought/Action/Observation | Sim | Não | Sim | Não | Investigar e agir com base em ferramentas e observações |
| Self-Consistency | Não | Não | Sim | Não | Não | Sim | Reduzir erro em tarefas com variação entre respostas |

### Diferenças práticas

| Técnica | O que ela adiciona | O que ela não substitui sozinha |
| --- | --- | --- |
| Zero-Shot | Rapidez e baixo custo de prompt | Controle fino de formato, investigação e validação adicional |
| Few-Shot | Demonstra o padrão exato que a resposta deve seguir | Raciocínio profundo, uso de ferramentas e consenso entre tentativas |
| Chain-of-Thought | Sequência lógica auditável antes da resposta final | Exploração de caminhos alternativos, ação no ambiente e votação por recorrência |
| Skeleton-of-Thought | Estrutura fixa para organizar a resposta antes da expansão | Investigação, uso de ferramentas e comparação entre hipóteses |
| Tree-of-Thought | Ramificação e comparação entre alternativas plausíveis | Consulta a sistemas externos e execução de ações reais |
| ReAct | Ciclo de pensamento, ação e observação com evidência externa | Escolha da melhor resposta por maioria e análise ampla de múltiplas estratégias |
| Self-Consistency | Seleção da resposta final mais recorrente entre tentativas independentes | Ferramentas externas, estrutura rígida e exploração deliberada de hipóteses |

### Exemplos do projeto

| Técnica | Exemplo no projeto | Por que encaixa |
| --- | --- | --- |
| Zero-Shot | Extração simples de dados de um CSV | A instrução direta já é suficiente para executar a tarefa |
| Few-Shot | Extração de CSV seguindo um formato ensinado por exemplos | O modelo aprende o padrão de saída antes de processar a entrada real |
| Chain-of-Thought | Extração de CSV com explicação passo a passo | O foco é tornar o raciocínio verificável antes da resposta final |
| Skeleton-of-Thought | Explicação de autenticação JWT em duas fases | Primeiro define a estrutura, depois expande cada tópico |
| Tree-of-Thought | Investigação de latência em API com múltiplas hipóteses | O problema pede exploração e comparação de caminhos antes da decisão |
| ReAct | Atendimento de suporte com verificação e desbloqueio de conta | O fluxo depende de consultar ferramentas, observar resultados e agir |
| Self-Consistency | Cálculo de reembolso por múltiplas resoluções independentes | A confiabilidade vem da recorrência da resposta final entre tentativas |
