# Política de Segurança / Security Policy

## 🇧🇷 Português

### Reportando uma vulnerabilidade

Se você identificou uma vulnerabilidade em qualquer repositório `fiscal-digital-*`, **não abra uma issue pública**. Reporte de forma reservada para que possamos coordenar a correção antes da divulgação.

**Canal preferido:** [GitHub Security Advisories](https://github.com/fiscal-digital/.github/security/advisories/new) (privado, integrado ao GitHub).

**Canal alternativo (e-mail):** `lineu@fiscaldigital.org` (endereço canônico de contato do projeto).

### O que incluir

- Repositório afetado e *commit*/branch
- Descrição da vulnerabilidade e impacto potencial
- Passos para reprodução (PoC se possível)
- Ambiente onde foi reproduzida (versão do Node, runtime AWS, etc.)
- Sua sugestão de mitigação, se houver

### O que esperar de nós

| Janela | Ação |
|---|---|
| 48 horas | Acuso de recebimento |
| 7 dias | Avaliação inicial e classificação de severidade |
| 90 dias | Janela padrão para correção e divulgação coordenada |

A janela de 90 dias é o padrão de *responsible disclosure*. Em casos críticos (chave/segredo exposto, RCE, dado sensível vazando) trabalhamos em janela mais curta.

### Escopo

Cobrem-se todos os repositórios sob a *org* [`fiscal-digital`](https://github.com/fiscal-digital):

- `fiscal-digital`
- `fiscal-digital-web`
- `fiscal-digital-collectors`
- `fiscal-digital-analytics`
- `fiscal-digital-evaluations`
- `.github` (este repo)

E os recursos AWS de produção (`fiscal-digital-*-prod`).

### Fora de escopo

- Vulnerabilidades em sistemas de terceiros que apenas consumimos (Querido Diário, Receita Federal, AWS) — reporte ao *upstream* correspondente.
- Conteúdo dos diários oficiais municipais — fonte original, fora do nosso controle. Erros de leitura ou interpretação geram **falso-positivo**, não vulnerabilidade — use o [template de falso positivo](https://github.com/fiscal-digital/.github/issues/new?template=falso_positivo.yml).

### Divulgação coordenada

Após a correção, publicamos:

- *Security Advisory* no GitHub com CVE quando aplicável
- *Release notes* descrevendo o problema e a versão corrigida
- Crédito público à pessoa que reportou (a menos que prefira anonimato)

### Hall of fame

Pesquisadores que contribuíram para a segurança do projeto via *responsible disclosure* recebem reconhecimento permanente nesta seção, no `README` da org, após a correção e divulgação coordenada.

*Nenhum reporte público até o momento.*

---

## 🇺🇸 English

### Reporting a vulnerability

If you identify a vulnerability in any `fiscal-digital-*` repository, **do not open a public issue**. Report it privately so we can coordinate a fix before disclosure.

**Preferred channel:** [GitHub Security Advisories](https://github.com/fiscal-digital/.github/security/advisories/new) (private, GitHub-native).

**Alternative (email):** `lineu@fiscaldigital.org` (the project's canonical contact address).

### What to include

Affected repo and commit/branch · vulnerability description and potential impact · reproduction steps (PoC if available) · environment where it was reproduced · your suggested mitigation, if any.

### What to expect from us

| Window | Action |
|---|---|
| 48 hours | Acknowledgment of receipt |
| 7 days | Initial assessment and severity classification |
| 90 days | Standard window for fix and coordinated disclosure |

The 90-day window is the standard responsible-disclosure timeline. Critical cases (exposed secrets, RCE, sensitive data leaks) are handled on a shorter window.

### Scope

All repositories under the [`fiscal-digital`](https://github.com/fiscal-digital) GitHub organization, plus production AWS resources (`fiscal-digital-*-prod`).

### Out of scope

Vulnerabilities in third-party systems we merely consume (Querido Diário, Receita Federal, AWS) — report upstream. Errors in the content of official gazettes themselves are not vulnerabilities — use the [false-positive template](https://github.com/fiscal-digital/.github/issues/new?template=falso_positivo.yml).

### Coordinated disclosure

After the fix is shipped, we publish: GitHub Security Advisory with CVE when applicable; release notes; public credit to the reporter (unless they prefer to remain anonymous).

### Hall of fame

Researchers who contributed to the project's security via responsible disclosure receive permanent acknowledgment in this section and in the org `README` after the coordinated disclosure.

*No public reports yet.*
