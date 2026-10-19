# Product — Documentação Centralizada

Este repositório centraliza a documentação normalizada do recurso **Products** (queries),
compartilhado pelos projetos [`node-express`](../node-express) e [`ruby-sinatra`](../ruby-sinatra)
da plataforma HTTP Pardal.

## Estrutura

| Caminho | Conteúdo |
|---------|----------|
| `docs/resources/product-queries.md` | Especificação normalizada do resource Products |
| `adr/` | Architecture Decision Records (decisões importantes) |

## Projetos consumidores

- `node-express` — consome via Git Submodule [`shared-configs`](../shared-configs)
- `ruby-sinatra` — consome via Git Submodule [`shared-configs`](../shared-configs)

O documento em `docs/resources/product-queries.md` é a fonte única da verdade
para o comportamento do resource Products. Ambos os projetos referenciam este
documento através do submodule `shared-configs`.