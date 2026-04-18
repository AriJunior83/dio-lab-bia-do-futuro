# Documentação do Agente

## Caso de Uso

### Problema
> Qual problema financeiro seu agente resolve?

Dificuldade em fazer investimento para alcançar a liberdade financeira.

### Solução
> Como o agente resolve esse problema de forma proativa?

Aplicativo para faciliar e gerenciar investimentos a longo prazo.

### Público-Alvo
> Quem vai usar esse agente?

Pessoas com dificuldade em fazer investimentos a longo prazo.

---

## Persona e Tom de Voz

### Nome do Agente
Ari

### Personalidade
> Como o agente se comporta? (ex: consultivo, direto, educativo)

Consultivo

### Tom de Comunicação
> Formal, informal, técnico, acessível?

Técnico

### Exemplos de Linguagem
- Saudação: [ex: "Olá! Como posso ajudar com suas finanças hoje?"]
- Confirmação: [ex: "Entendi! Deixa eu verificar isso para você."]
- Erro/Limitação: [ex: "Não tenho essa informação no momento, mas posso ajudar com..."]

---

## Arquitetura

### Diagrama

```mermaid
flowchart TD
    A[Cliente] -->|Mensagem| B[Interface]
    B --> C[LLM]
    C --> D[Base de Conhecimento]
    D --> C
    C --> E[Validação]
    E --> F[Resposta]
```

### Componentes

| Componente | Descrição |
|------------|-----------|
| Interface | [ex: Chatbot em Streamlit] |
| LLM | [ex: GPT-4 via API] |
| Base de Conhecimento | [ex: JSON/CSV com dados do cliente] |
| Validação | [ex: Checagem de alucinações] |

---

## Segurança e Anti-Alucinação

### Estratégias Adotadas

- [ ] [Agente só responde com base nos dados fornecidos]
- [ ] [Respostas incluem fonte da informação]
- [ ] [Quando não sabe, admite e redireciona]
- [ ] [Não faz recomendações de investimento sem perfil do cliente]

### Limitações Declaradas
> O que o agente NÃO faz?
Não faz investimento automaticamente. apenas faz recomendações.
