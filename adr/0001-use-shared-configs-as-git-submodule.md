# ADR 0001 — Usar shared-configs como Git Submodule

## Status

Aceito

## Contexto

Os projetos `node-express` e `ruby-sinatra` duplicavam os mesmos arquivos de contrato
(`contract/database.sql`, `contract/openapi.yml`), seeds (`seeds/*.yml`) e documentação
(`docs/resources/*.md`). Manter essas cópias sincronizadas manualmente gerava risco de
desvio (drift) entre as implementações.

## Decisão

Criar o repositório `shared-configs` como fonte única desses arquivos compartilhados e
referenciá-lo como Git Submodule em ambos os projetos:

- `node-express/shared-configs`
- `ruby-sinatra/shared-configs`

Os submodules são inicializados com `git submodule update --init` e os CI são
configurados com `submodules: true` no `actions/checkout`.

## Consequências

### Positivas

- Fonte única da verdade para contrato e seeds; alterações refletem em ambos os projetos
  simultaneamente.
- Eliminação de arquivos duplicados (~12 arquivos removidos de cada projeto).
- CI garante que o submodule seja baixado antes de rodar testes/lint.

### Negativas / Trade-offs

- Clones dos projetos exigem um passo extra (`git submodule update --init`).
- Alterações no submodule exigem commit em dois repositórios (submodule + projeto pai).
- Caminhos internos dos projetos precisaram ser atualizados para `shared-configs/...`.

## Relacionados

- ADR 0002 — Preservar diferenças de dialeto SQL no `database.sql` compartilhado
- ADR 0003 — Manter carregadores de seed específicos de cada linguagem fora do submodule
- ADR 0004 — Criar repositório `product` para documentação centralizada