# ADR 0003 — Manter carregadores de seed específicos de cada linguagem fora do submodule

## Status

Aceito

## Contexto

Os arquivos de dados das seeds (`users.yml`, `products.yml`, `payments.yml`) são idênticos
entre `node-express` e `ruby-sinatra` e foram movidos para `shared-configs/seeds/`.
No entanto, o código que carrega e interpreta esses dados difere entre as linguagens:

- **node-express:** `db/seeds/index.js` + `db/seeds/load-list.js` +
  `db/seeds/loaders/{users,products,payments}.js` (Prisma + bcryptjs).
- **ruby-sinatra:** `db/seeds.rb` (ActiveRecord + YAML.safe_load_file).

## Decisão

Mover apenas os arquivos YAML de dados para o submodule (`shared-configs/seeds/`).
Manter os carregadores (lógica de leitura, hashing de senha, idempotência por email/nome/amount)
dentro de cada projeto, nos caminhos originais, sem alterar funcionalidades.

## Consequências

### Positivas

- Dados de seed sincronizados via submodule.
- Lógica específica de cada linguagem (bcrypt vs ActiveRecord, Prisma vs SQL) preservada.
- Nenhuma mudança de comportamento na carga de seeds.

### Negativas / Trade-offs

- Dois locais para alterar se a estrutura dos dados de seed mudar (arquivo YAML no
  submodule + possivelmente loader se a interpretação mudar).

## Relacionados

- ADR 0001 — Usar shared-configs como Git Submodule