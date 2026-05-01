<!--
  Fiscal Digital — Pull Request Template
  Antes de abrir o PR, leia: CONTRIBUTING.md
  Before opening, read: CONTRIBUTING.md
-->

## Resumo da mudança / Summary

<!-- 1-3 linhas factuais sobre o que muda e por quê.
     1-3 factual lines describing what changes and why. -->

## Issue relacionada / Related issue

<!-- Closes #123  —  ou descreva por que não há issue.
     Closes #123  —  or explain why there is no issue. -->

## Como testar / How to test

<!-- Passos numerados que um revisor possa seguir.
     Numbered steps a reviewer can follow.

     Exemplo / Example:
     1. `git fetch && git checkout <branch>`
     2. `npm install && npm run type-check`
     3. ... -->

## Tipo de mudança / Type of change

<!-- Marque uma opção / Pick one -->

- [ ] *Bug fix* — corrige comportamento incorreto / fixes incorrect behavior
- [ ] *Feature* — nova funcionalidade / new functionality
- [ ] *Refactor* — sem mudança de comportamento / no behavioral change
- [ ] *Docs* — documentação, READMEs, brand pack / documentation, READMEs, brand pack
- [ ] *Infra/CI* — Terraform, GitHub Actions, OIDC, IAM
- [ ] *Lógica de Fiscal Agente* — regra de detecção, *threshold*, base legal aplicada / Fiscal Agent logic — detection rule, threshold, applied legal basis
- [ ] *Copy / voz* — texto público, prompts, narrativas / public copy, prompts, narratives
- [ ] *Brand pack* — cores, glossário, logos, social / brand pack assets

## Checklist obrigatória / Required checklist

- [ ] Testes passam localmente (`npm run type-check` ou equivalente do repo). / Tests pass locally.
- [ ] *Lint*/formatação OK. / Lint and formatting OK.
- [ ] Commits seguem o padrão (assunto curto, corpo explica o **porquê**, sem `Co-Authored-By: Claude`). / Commits follow the standard (short subject, body explains **why**, no `Co-Authored-By: Claude`).
- [ ] Não introduzi termos da [`glossary.json#avoid`](https://github.com/fiscal-digital/fiscal-digital-web/blob/main/brand/glossary.json) em conteúdo público. / I did not introduce any `glossary.json#avoid` term into public content.
- [ ] Não estou *commitando* segredos, *tokens* ou Account IDs. / I am not committing secrets, tokens or AWS Account IDs.
- [ ] Mudei *dependencies*? Justifiquei na descrição. / If I changed dependencies, I justified it above.

## Se a mudança altera lógica de Fiscal Agente — obrigatório / If this changes Fiscal Agent logic — required

- [ ] Incluí a **base legal** (lei + artigo) que justifica a regra. / Included the **legal basis** (law + article).
- [ ] Incluí um exemplo (gazette/ato, *fixture* ou trecho) que **dispara** o alerta. / Included an example that **triggers** the alert.
- [ ] Incluí um exemplo que **NÃO** dispara — falso positivo evitado. / Included an example that does **not** trigger — false positive avoided.

## Se a mudança altera copy ou voz / If this changes copy or voice

- [ ] Segui o [`brand/voice-tone.md`](https://github.com/fiscal-digital/fiscal-digital-web/blob/main/brand/voice-tone.md) (factual, sóbrio, técnico, nunca acusatório). / I followed `voice-tone.md` (factual, sober, technical, never accusatory).
- [ ] Termos PT↔EN seguem o [`brand/glossary.json`](https://github.com/fiscal-digital/fiscal-digital-web/blob/main/brand/glossary.json) — em particular: `secretaria → municipal department`, `fiscalização → oversight`. / Terms follow `glossary.json` — in particular `secretaria → municipal department`, `fiscalização → oversight`.

## Se a mudança altera brand pack / If this changes the brand pack

- [ ] PR aberto no `fiscal-digital-web` (owner canônico). / PR opened in `fiscal-digital-web` (canonical owner).
- [ ] Após editar SVG, regerei os PNGs derivados conforme `brand/README.md`. / After editing SVGs, I rebuilt the derived PNGs per `brand/README.md`.
- [ ] Mudanças que afetem o contrato de consumo (`glossary.json`, `colors.json`, estrutura de `risk`) foram coordenadas com os repos consumidores. / Changes affecting the consumer contract were coordinated with downstream repos.

## Notas para o revisor / Notes for the reviewer

<!-- Áreas em que você gostaria de atenção especial, dúvidas em aberto, decisões de design.
     Areas you would like extra attention on, open questions, design decisions. -->
