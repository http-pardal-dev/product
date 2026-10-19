# ADR 0004 — Criar repositório product para documentação centralizada

## Status

Aceito

## Contexto

A documentação do recurso Products (`product-queries.md`) existia separadamente em
`node-express/docs/resources/` e `ruby-sinatra/docs/resources/`, com conteúdo quase
idêntico mas referências de código específicas de cada linguagem (`src/` vs `app/`,
`prisma/schema.prisma` vs `db/migrate/`). Após a refatoração para `shared-configs`,
esse documento ficou apenas no submodule, sem um repositório dedicado para evoluí-lo
de forma independente dos projetos consumidores.

## Decisão

Criar o repositório `product` contendo:

- `docs/resources/product-queries.md` — versão normalizada (single source of truth),
  sem referências de código específicas de linguagem.
- `adr/` — registros de decisões de arquitetura (este ADR e os relacionados).
- `README.md` — visão geral e projetos consumidores.

O `shared-configs/docs/resources/product-queries.md` continua sendo a cópia consumida
pelos projetos via submodule; o repositório `product` é o local de edição e revisão
da documentação antes de ser espelhada no `shared-configs`.

## Consequências

### Positivas

- Documentação do Products centralizada e versionada independentemente dos projetos.
- ADRs registram decisões de arquitetura para consulta futura.
- Padronização de terminologia (ex.: `min_price`/`max_price`, `price` como texto na rede).

### Negativas / Trade-offs

- Mais um repositório para manter; exige processo de espelhamento para `shared-configs`.

## Relacionados

- ADR 0001 — Usar shared-configs como Git Submodule