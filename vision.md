# HTTP Pardal — Visão do Produto

## 1. Visão

O HTTP Pardal é um conjunto de ambientes práticos para explorar, testar e experimentar HTTP e APIs sem precisar construir uma aplicação do zero.

O projeto oferece APIs prontas para execução, organizadas em cenários que permitem interagir com recursos, observar respostas, experimentar operações e compreender o comportamento de uma aplicação backend na prática.

**A ideia central é reduzir o tempo entre querer experimentar uma API e começar a utilizá-la.**

## 2. Problema

Aprender e experimentar HTTP e APIs pode exigir uma preparação desproporcional ao objetivo do usuário.

Mesmo para testar uma requisição simples, pode ser necessário configurar um projeto, instalar dependências, implementar endpoints, preparar um banco de dados e resolver problemas que não fazem parte do conceito que se deseja explorar.

Isso cria uma barreira entre a curiosidade e a prática.

O HTTP Pardal busca reduzir essa barreira, oferecendo ambientes previamente preparados, com comportamentos definidos e instruções claras para começar.

## 3. Público-alvo

O projeto é destinado a pessoas que desejam experimentar HTTP e APIs na prática, especialmente:

* Iniciantes em desenvolvimento web e backend.
* Estudantes que desejam complementar seus estudos.
* Desenvolvedores que querem testar requisições e respostas HTTP.
* Pessoas que estão conhecendo ferramentas como cURL, Postman e Insomnia.
* Desenvolvedores interessados em explorar diferentes linguagens e frameworks.

O produto deve ser acessível a quem ainda não domina a implementação de servidores.

## 4. Proposta de valor

O HTTP Pardal oferece ambientes prontos para uso que permitem concentrar o esforço na experimentação, em vez de na preparação da infraestrutura.

Seus principais benefícios são:

* **Prática imediata:** começar a experimentar sem desenvolver uma API do zero.
* **Simplicidade:** executar os ambientes com instruções claras e poucos passos.
* **Exploração:** experimentar requisições, parâmetros, cabeçalhos, respostas e estados.
* **Previsibilidade:** trabalhar com comportamentos e dados iniciais conhecidos.
* **Recuperação:** restaurar o estado inicial e repetir os experimentos.
* **Acessibilidade:** utilizar ferramentas HTTP comuns, sem depender de uma interface proprietária.
* **Variedade:** explorar cenários semelhantes implementados em diferentes linguagens e frameworks.

## 5. Experiência principal

A experiência do produto é organizada em um ciclo simples:

**PREPARAR → EXECUTAR → EXPERIMENTAR → RESTAURAR**

1. **Preparar:** escolher um ambiente e seguir as instruções de inicialização.
2. **Executar:** iniciar a API e conectar-se a ela por meio de uma ferramenta HTTP.
3. **Experimentar:** enviar requisições, observar respostas, modificar parâmetros e explorar comportamentos.
4. **Restaurar:** retornar ao estado inicial quando necessário e começar novos experimentos.

O usuário deve conseguir chegar rapidamente à parte mais importante: interagir com a API.

## 6. Cenários práticos

Os ambientes utilizam cenários concretos para tornar os conceitos HTTP observáveis.

### Users

Operações com usuários permitem explorar:

* Operações CRUD.
* Métodos HTTP.
* Parâmetros de rota.
* Validação de dados.
* Códigos de status e tratamento de erros.

### Products

Operações com produtos permitem explorar:

* Parâmetros de consulta.
* Filtros e ordenação.
* Paginação.
* Consultas e recuperação de recursos.

### Payments

Operações com pagamentos permitem explorar:

* Ciclo de vida de um recurso.
* Transições de estado.
* Ações específicas.
* Atualizações e validações.
* Comportamentos associados às operações.

Esses cenários servem como exemplos práticos. O objetivo não é simular integralmente um sistema comercial, mas disponibilizar comportamentos suficientemente concretos para experimentação.

## 7. Princípios do produto

### 7.1. A prática vem primeiro

A experiência deve priorizar a interação direta com as APIs.

Explicações e materiais didáticos podem complementar os ambientes, mas não devem se tornar uma barreira para utilizá-los.

### 7.2. Simplicidade operacional

Os ambientes devem ser fáceis de instalar, iniciar, testar e restaurar.

Dependências e etapas desnecessárias devem ser evitadas.

### 7.3. Clareza antes de abstração

O código deve ser legível, organizado e compreensível.

Abstrações complexas não devem ser introduzidas sem uma necessidade concreta.

### 7.4. Consistência entre implementações

Diferentes linguagens e frameworks devem oferecer experiências equivalentes.

Os contratos HTTP, os cenários, os recursos e os comportamentos esperados devem permanecer consistentes, enquanto cada implementação pode seguir as convenções de sua tecnologia.

### 7.5. Experimentação segura e repetível

O usuário deve conseguir testar operações, observar resultados, cometer erros e restaurar os dados sem precisar reconstruir o ambiente.

### 7.6. Independência de ferramentas

As APIs devem poder ser utilizadas com ferramentas HTTP comuns, sem exigir uma interface gráfica específica do HTTP Pardal.

### 7.7. Evolução gradual

O projeto deve crescer de acordo com necessidades concretas.

Novos cenários, tecnologias e recursos devem ser adicionados sem comprometer a simplicidade dos ambientes existentes.

## 8. Direção do produto

O HTTP Pardal deve evoluir como um catálogo organizado de ambientes práticos para explorar HTTP e APIs.

O site público será responsável por apresentar o produto, facilitar a descoberta dos ambientes, explicar seus objetivos e orientar o usuário até a execução.

Cada ambiente terá sua própria implementação e instruções, mantendo contratos e experiências consistentes com o restante do catálogo.

O projeto prioriza a utilidade prática e a facilidade de uso, evitando transformar os ambientes em aplicações de produção ou plataformas excessivamente complexas.

## 9. Escopo e limites

O HTTP Pardal não tem como objetivo principal:

* Substituir cursos, livros ou documentação oficial.
* Oferecer APIs comerciais para aplicações de produção.
* Construir uma plataforma completa de desenvolvimento backend.
* Exigir que o usuário implemente uma API antes de poder experimentá-la.
* Reproduzir toda a complexidade de sistemas empresariais.
* Introduzir infraestrutura externa quando ela não for necessária para o cenário.

Os ambientes devem permanecer focados nos comportamentos que tornam a experimentação útil.

## 10. Acessibilidade e sustentabilidade

Os ambientes devem ser disponibilizados gratuitamente para uso prático e exploratório, com código público e instruções acessíveis.

A sustentabilidade do projeto poderá ser apoiada por contribuições voluntárias e outras iniciativas compatíveis com sua proposta aberta e acessível.

Essas iniciativas não devem comprometer o acesso aos ambientes essenciais.

## 11. Critério de sucesso

O HTTP Pardal estará cumprindo sua proposta quando uma pessoa conseguir:

1. Encontrar rapidamente um ambiente adequado ao que deseja experimentar.
2. Entender o que aquele ambiente permite explorar.
3. Prepará-lo sem enfrentar complexidade desnecessária.
4. Interagir com a API utilizando ferramentas conhecidas.
5. Compreender os resultados observados.
6. Restaurar o ambiente e repetir os experimentos.

**O sucesso do produto não depende da quantidade de tecnologias ou funcionalidades disponíveis, mas da facilidade com que as pessoas conseguem passar da intenção à experimentação prática.**

---

*Este documento define a visão e os princípios do HTTP Pardal. Detalhes de implementação, prioridades de desenvolvimento e decisões técnicas devem ser documentados separadamente.*
