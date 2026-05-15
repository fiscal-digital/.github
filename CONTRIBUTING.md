# Contribuindo com o Fiscal Digital

Obrigado pelo interesse em contribuir. O Fiscal Digital é uma iniciativa cívica aberta — toda contribuição passa por revisão pública e fica auditável para sempre no histórico do Git.

---

## 🇧🇷 Português

### Workflow

```
Issue pública → discussão → fork → PR → review → merge
```

1. **Abra uma issue antes de codar.** Especialmente para mudanças não triviais. Discutir antes economiza retrabalho.
2. **Faça um fork** e crie um *branch* descritivo (`fix/cnpj-validator`, `feat/fiscal-licitacoes-fracionamento`).
3. **Implemente** seguindo as regras de PR abaixo.
4. **Abra o PR** com o template preenchido. Linke a issue.
5. **Review e merge** acontecem em público.

### Repositórios

Cada repo tem o seu `README.md` com instruções de *setup* local:

- [`fiscal-digital`](https://github.com/fiscal-digital/fiscal-digital) — engine, Fiscais, Terraform
- [`fiscal-digital-web`](https://github.com/fiscal-digital/fiscal-digital-web) — site, **owner do brand pack**
- [`fiscal-digital-collectors`](https://github.com/fiscal-digital/fiscal-digital-collectors) — adaptadores de fontes
- [`fiscal-digital-analytics`](https://github.com/fiscal-digital/fiscal-digital-analytics) — notebooks e exports
- [`fiscal-digital-evaluations`](https://github.com/fiscal-digital/fiscal-digital-evaluations) — golden set rotulado e ADRs por Fiscal

Stack comum: TypeScript *strict*, Node.js 24.x, AWS *serverless*. Detalhes por repo.

### Regra dura — PR que altera lógica de Fiscal

Um Fiscal é um agente autônomo que decide se publica um alerta sobre dinheiro público. **Mudanças na lógica de qualquer Fiscal** (regras de detecção, *thresholds*, base legal aplicada) exigem, no PR:

1. **Referência legal** — lei e artigo que justifica a regra. Ex.: *Lei 14.133/2021, Art. 75 (teto de R$ 100k para obras em dispensa de licitação)*.
2. **Exemplo de gazette/ato que dispara o alerta** — trecho real (ou *fixture* fiel) que a regra deve flagar. Idealmente com URL do diário no Querido Diário.
3. **Exemplo que NÃO deve disparar** — caso de borda que poderia parecer suspeito mas é legítimo. Documentar o falso positivo evitado.

PR sem os três itens acima é bloqueado. Não é burocracia — é o que mantém o projeto verificável.

### Mudanças em copy ou voz

Toda comunicação pública (site, alertas, READMEs, narrativas geradas pelo Haiku) segue o **Voice & Tone Guide** do brand pack:

- Princípios e DO/DON'T bilíngue: [`fiscal-digital-web/brand/voice-tone.md`](https://github.com/fiscal-digital/fiscal-digital-web/blob/main/brand/voice-tone.md)
- Termos PT↔EN canônicos: [`fiscal-digital-web/brand/glossary.json`](https://github.com/fiscal-digital/fiscal-digital-web/blob/main/brand/glossary.json)

A lista [`glossary.json#avoid`](https://github.com/fiscal-digital/fiscal-digital-web/blob/main/brand/glossary.json) contém **termos proibidos** em conteúdo público — `fraude`, `desvio`, `esquema`, `corrupção` e outros. O *publisher* da engine rejeita automaticamente *posts* que contenham qualquer um deles. Isso é deliberado: é mais barato regenerar do que retratar.

PRs em copy/voz que precisem incluir um termo da lista `avoid` por motivo legítimo (ex.: documentação interna sobre por que o termo é proibido) devem deixar isso explícito na descrição.

### Mudanças no brand pack

O `fiscal-digital-web` é o *owner* canônico do brand pack. Se a sua mudança afeta cores, glossário ou *voice-tone*, o PR vai naquele repo. Outros repos consomem via `gh api` em *build-time* — quebrar o contrato quebra produção.

### Estilo de código

- TypeScript *strict mode* — sem `any` implícito
- Nomes de recursos AWS: `kebab-case` minúsculas, padrão `fiscal-digital-<nome>-prod`
- Commits: assunto curto (≤72 chars), corpo explicando o **porquê**, não o **o quê**
- **Sem `Co-Authored-By: Claude`** ou similares em commits — créditos só para contribuidores humanos
- Sempre commitar **todos** os arquivos relacionados a uma mudança — *commit* parcial quebra `terraform apply` no CI

### Princípios inegociáveis

Toda contribuição respeita:

- **Sempre citar a fonte** — todo achado aponta para o diário original
- **Não acusar, informar** — linguagem factual, nunca acusatória
- **Transparência do algoritmo** — cada alerta explica por que foi gerado
- **Verificabilidade pública** — qualquer cidadão pode checar a fonte
- **Retratação pública** — erro publicado = correção no mesmo canal e alcance

### Reportando problemas

- **Bug ou comportamento inesperado:** [issue de bug](https://github.com/fiscal-digital/.github/issues/new?template=bug_report.yml)
- **Nova *feature*, Fiscal, *skill* ou fonte de dados:** [issue de feature](https://github.com/fiscal-digital/.github/issues/new?template=feature_request.yml)
- **Alerta publicado incorreto:** [issue de falso positivo](https://github.com/fiscal-digital/.github/issues/new?template=falso_positivo.yml) — ativa o processo de retratação pública
- **Vulnerabilidade de segurança:** **NÃO abra issue pública** — siga [`SECURITY.md`](SECURITY.md)

### Código de Conduta

Toda interação no projeto segue o [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) (Contributor Covenant 2.1).

---

## 🇺🇸 English

### Workflow

```
Public issue → discussion → fork → PR → review → merge
```

Open an issue before non-trivial work. Fork, branch, implement, PR with the template filled in. Review and merge happen in public.

### Hard rule — PRs that change Fiscal Agent logic

A Fiscal Agent decides whether to publish an alert about public money. **Any change to a Fiscal's detection logic, thresholds, or applied legal basis** must include in the PR:

1. **Legal basis** — law and article that justifies the rule (e.g., *Law 14.133/2021, Article 75*).
2. **A gazette excerpt that should trigger the alert** — real or faithful fixture, ideally with a Querido Diário URL.
3. **An example that should NOT trigger** — an edge case that looks suspicious but is legitimate. Document the false positive avoided.

PRs missing any of the three are blocked. It is what keeps the project verifiable.

### Copy and voice changes

All public communication follows the brand pack's [Voice & Tone Guide](https://github.com/fiscal-digital/fiscal-digital-web/blob/main/brand/voice-tone.md). Public posts must avoid the [`glossary.json#avoid`](https://github.com/fiscal-digital/fiscal-digital-web/blob/main/brand/glossary.json) list (`fraud`, `embezzlement`, `scheme`, `corruption`, etc.) — the publisher rejects them automatically.

### Brand pack

`fiscal-digital-web` is the canonical owner. Brand changes go there. Other repos consume the brand pack at build time — breaking the contract breaks production.

### Code style

- TypeScript strict mode
- AWS resources: lowercase `kebab-case`, pattern `fiscal-digital-<name>-prod`
- Commits: short subject, body explains **why**, not **what**
- **No `Co-Authored-By: Claude`** lines — credit only human contributors
- Always commit all related files — partial commits break `terraform apply` in CI

### Reporting

- Bug → bug report template
- Feature/Fiscal/skill/data source → feature request template
- **Incorrect published alert** → false-positive template (triggers our public retraction process)
- Security vulnerability → see [`SECURITY.md`](SECURITY.md), do not open a public issue

### Code of Conduct

All interaction follows [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) (Contributor Covenant 2.1).
