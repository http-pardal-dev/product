# ADR 0002 — Preservar diferenças de dialeto SQL no database.sql compartilhado

## Status

Aceito

## Contexto

O arquivo `contract/database.sql` descreve o mesmo esquema (users, products, payments)
para ambos os projetos, mas cada ORM mapeia tipos diferente:

- **node-express (Prisma):** `TEXT`, `DATETIME ... DEFAULT CURRENT_TIMESTAMP`,
  índice único separado (`users_email_key`).
- **ruby-sinatra (ActiveRecord):** `VARCHAR`, `DATE`, `DECIMAL(10, 2)`,
  `CONSTRAINT ... UNIQUE` inline, sem defaults de coluna.

## Decisão

Manter um único `database.sql` no `shared-configs` que documente ambas as variações
como comentários, preservando as diferenças de dialeto em vez de unificá-las forçosamente.
Cada projeto continua usando seu próprio DDL gerado (Prisma migrations / ActiveRecord
migrations); o `database.sql` serve como referência contratual compartilhada.

## Consequências

### Positivas

- Nenhuma alteração de comportamento nos bancos de dados existentes.
- Documentação contratual sincronizada sem forçar uniformização de tipos.

### Negativas / Trade-offs

- O arquivo compartilhado não é executável diretamente em ambos os ORMs sem adaptação;
  ele é referência, não DDL fonte geradora.

## Relacionados

- ADR 0001 — Usar shared-configs como Git Submodule