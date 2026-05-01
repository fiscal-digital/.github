<p align="center">
  <img src="https://raw.githubusercontent.com/fiscal-digital/fiscal-digital-web/main/brand/logo/symbol.svg" width="96" alt="Fiscal Digital" />
</p>

# Fiscal Digital

> Agente autônomo de fiscalização de gastos públicos municipais no Brasil.
> Transformamos dados públicos em alertas verificáveis para a sociedade.

[![Código MIT](https://img.shields.io/badge/c%C3%B3digo-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Dados CC-BY 4.0](https://img.shields.io/badge/dados-CC--BY%204.0-orange.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Status: MVP em desenvolvimento](https://img.shields.io/badge/status-MVP%20em%20desenvolvimento-yellow.svg)]()

---

## O que é

Um agente autônomo que monitora diários oficiais de prefeituras brasileiras e identifica indícios de irregularidades em gastos públicos. Cada alerta publicado é factual, cita a fonte original e referencia a base legal.

**Primeira cobertura:** Caxias do Sul (RS) — gestão 2021 em diante.

## Como funciona

1. **Coleta** — busca novos diários no [Querido Diário (OKFN Brasil)](https://queridodiario.ok.org.br) todos os dias
2. **Análise** — fiscais especializados (licitações, contratos, fornecedores, pessoal) cruzam dados, validam CNPJs, checam sanções (CGU)
3. **Publicação** — achados de risco alto vão automaticamente para [@LiFiscalDigital](https://x.com/LiFiscalDigital)

## Princípios inegociáveis

| | |
|---|---|
| 🔗 **Sempre citar a fonte** | Todo alerta linka para o diário original |
| 📰 **Não acusar, informar** | Linguagem factual, nunca acusatória |
| 🔍 **Transparência do algoritmo** | Cada alerta explica por que foi gerado |
| 🤝 **Verificabilidade pública** | Qualquer pessoa pode checar a fonte |
| ✏️ **Retratação pública** | Erro = correção no mesmo canal e alcance |

## Inspiração e ecossistema

Fiscal Digital nasce sobre os ombros de dois projetos fundamentais da inovação cívica brasileira:

- **[Serenata de Amor](https://serenata.ai)** — pioneira no uso de IA para fiscalizar gastos públicos no Brasil (CEAP federal)
- **[Querido Diário](https://queridodiario.ok.org.br)** — infraestrutura que digitalizou diários oficiais municipais

Não competimos — estendemos. Todo achado linka para o Querido Diário. Sem ele, este projeto não existiria.

## Repositórios

| Repo | Conteúdo |
|---|---|
| [`fiscal-digital`](https://github.com/fiscal-digital/fiscal-digital) | Engine: Fiscais + Skills + API (TypeScript serverless na AWS) |
| [`fiscal-digital-web`](https://github.com/fiscal-digital/fiscal-digital-web) | Landing + dashboards por cidade (Next.js). **Owner do brand pack.** |
| [`fiscal-digital-collectors`](https://github.com/fiscal-digital/fiscal-digital-collectors) | Adaptadores de fontes de dados |
| [`fiscal-digital-analytics`](https://github.com/fiscal-digital/fiscal-digital-analytics) | Notebooks, relatórios e exports |

## Onde nos encontrar

- 🌐 Site (em construção): [fiscaldigital.org](https://fiscaldigital.org)
- 🐦 X institucional: [@FiscalDigitalBR](https://x.com/FiscalDigitalBR)
- 🤖 Bot Lineu (publica alertas): [@LiFiscalDigital](https://x.com/LiFiscalDigital)

## Quero contribuir

Issues e PRs são bem-vindos. PR que altera lógica de Fiscal exige:

1. **Referência legal** (lei + artigo)
2. **Exemplo de gazette** que dispara o alerta
3. **Exemplo de gazette** que NÃO deve disparar (falso positivo evitado)

Veja [`CONTRIBUTING.md`](https://github.com/fiscal-digital/.github/blob/main/CONTRIBUTING.md) antes de abrir o primeiro PR.

## Errei? Erre comigo

Alerta incorreto: abra uma [issue de falso positivo](https://github.com/fiscal-digital/.github/issues/new?template=falso_positivo.yml). Publicamos correção nas mesmas redes com o mesmo alcance do alerta original.

## Licenças

- **Código:** MIT (todos os repos `fiscal-digital-*`)
- **Brand pack, dados e alertas:** CC-BY 4.0

---

## 🇺🇸 English (summary)

**Fiscal Digital** is a non-partisan, non-governmental civic initiative.

Autonomous agents read Brazilian municipal official gazettes and turn public data into verifiable alerts for society. Every alert cites its source. Every algorithm is auditable. Any error is corrected in the same channel and reach as the original publication.

First coverage: **Caxias do Sul (RS, Brazil)** — Adiló Didomenico administration (2021–present).

### Standing on shoulders

Fiscal Digital stands on the shoulders of two foundational Brazilian civic-tech projects:

- **[Serenata de Amor](https://serenata.ai)** (Open Knowledge Foundation Brazil) — pioneered the use of AI to oversee Brazilian federal spending since 2016.
- **[Querido Diário](https://queridodiario.ok.org.br)** (Open Knowledge Foundation Brazil) — infrastructure that digitized official gazettes from hundreds of Brazilian municipalities. Our primary data source.

We don't compete. **We extend.** Every finding links back to Querido Diário. We never duplicate the data.

### Repositories · Status · Contributing

The 4 public repos under this org are described in the Portuguese section above. Status: **under development** — public launch conditional on the fiscal pipeline generating real alerts for the first covered city.

To contribute, read [`CONTRIBUTING.md`](https://github.com/fiscal-digital/.github/blob/main/CONTRIBUTING.md). PRs that change Fiscal Agent logic require legal basis + a triggering example + a non-triggering example.

### Contact

Website: [fiscaldigital.org](https://fiscaldigital.org) · X: [@FiscalDigitalBR](https://x.com/FiscalDigitalBR) (institutional) · [@LiFiscalDigital](https://x.com/LiFiscalDigital) (Lineu bot, alert publisher)

### Licenses

- **Code:** MIT
- **Brand pack, data and alerts:** CC-BY 4.0 (free use, with attribution)

---

*Projeto open source mantido por [@vieiradiego](https://github.com/vieiradiego) e contribuidores.*
*Open source project maintained by [@vieiradiego](https://github.com/vieiradiego) and contributors.*
