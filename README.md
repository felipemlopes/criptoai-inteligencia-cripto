# CriptoAI — Inteligência de mercado cripto com IA

> Plataforma de análise de criptoativos: scanner de oportunidades, smart money, mapa de liquidez, tendência e novas listagens, em um painel com planos e créditos.

![Laravel](https://img.shields.io/badge/Laravel-FF2D20?logo=laravel&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Gemini](https://img.shields.io/badge/Google%20Gemini-8E75B2?logo=googlegemini&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)

> **Repositório vitrine.** O código-fonte é proprietário (FML Tech) e fica privado. Aqui estão o problema, a arquitetura e as decisões técnicas. Demonstração técnica disponível sob solicitação.

## O problema

Quem investe em cripto precisa juntar dados de várias fontes para entender para onde o dinheiro está indo. A CriptoAI reúne esses sinais em um painel único e usa IA para interpretar o mercado. Também é oferecida em white-label, para criadores de conteúdo do nicho terem a ferramenta com a própria marca.

## O que o sistema faz

- **Scanner de oportunidades** e **scanner gráfico**
- **Smart money**: acompanhamento de fluxo de grandes carteiras
- **Mapa de liquidez** e **análise de tendência**
- **Novas listagens**, ICOs e airdrops
- **Dados on-chain**
- **Análises com IA** (Google Gemini)
- **Planos, assinaturas e pacotes de créditos**, com carteira interna e histórico de transações
- **Academy**: conteúdo educacional dentro da plataforma

## Arquitetura

```mermaid
flowchart LR
    FE[Painel · Next.js] --> API[API · Laravel]
    API --> SRV[Serviços de análise: scanner, smart money, liquidez, tendência]
    SRV --> EXT[APIs de mercado]
    API --> IA[Google Gemini]
    API --> BILL[Cobrança: planos, créditos e carteira]
    API --> DB[(MySQL)]
```

- Frontend e API em repositórios separados, cada um com Docker para produção.
- Cada análise é um **serviço isolado** no backend, o que permite ligar e desligar módulos por plano.
- A cobrança por **créditos** controla o consumo das análises mais caras.

## Stack

| Camada | Tecnologias |
|---|---|
| Backend | PHP 8.2, Laravel, Sanctum, carteira digital (bavix/laravel-wallet) |
| IA | Google Gemini |
| Frontend | Next.js, React, TypeScript, Tailwind, Radix UI |
| Infra | Docker, Docker Compose, GitHub Actions |

## Status

Produto da FML Tech, oferecido também em white-label.

## Autor

**Felipe Lopes** · Full-stack e fundador da [FML Tech](https://fmlsoftware.com.br)
Produto, backend e integrações de dados e IA.
