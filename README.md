# DESAFIO-QA-BEEDOO-2026

## 1. Objetivo do desafio

Este repositório contém a análise, documentação de testes e registro de bugs referentes ao desafio técnico para a vaga de **Analista de Qualidade Jr - Beedoo**.

A aplicação analisada disponibiliza funcionalidades para **cadastro, listagem e exclusão de cursos**.

O objetivo deste desafio foi avaliar a aplicação sob a perspectiva de qualidade de software, identificando fluxos principais, possíveis falhas e propondo cenários de teste que garantam o correto funcionamento do sistema.

---

# 2. Análise inicial da aplicação

A aplicação analisada consiste em um módulo simples de gerenciamento de cursos.

O sistema permite que o usuário:

* Cadastre um curso
* Visualize cursos cadastrados
* Exclua cursos da lista

O fluxo principal da aplicação está concentrado no formulário de cadastro e na listagem de cursos cadastrados.

---

# 3. Principais fluxos identificados

Durante a exploração da aplicação foram identificados os seguintes fluxos principais:

### Cadastro de curso

1. Acessar a tela de cadastro
2. Preencher os campos do formulário
3. Enviar o formulário
4. O curso é adicionado à lista

### Listagem de cursos

1. Acessar a tela de listagem
2. Visualizar cursos cadastrados
3. Ver informações como:

   * Nome do curso
   * Tipo
   * Datas
   * Número de vagas

### Exclusão de curso

1. Selecionar um curso da lista
2. Acionar a opção de exclusão
3. Receber confirmação da ação

---

# 4. Pontos considerados críticos para teste

Durante a análise foram identificados alguns pontos de maior impacto para a qualidade do sistema:

* Validação dos campos do formulário
* Coerência entre data de início e data de fim
* Cadastro com campos vazios
* Persistência dos dados na listagem
* Funcionamento da exclusão de cursos
* Feedback visual ao usuário
* Responsividade da interface
* Tratamento de entradas inválidas ou inesperadas

---

# 5. Estratégia utilizada para criação dos testes

Considerando o escopo da aplicação, os testes foram organizados com foco em:

* Fluxo principal de cadastro
* Cenários negativos
* Validações de campos
* Comportamentos inesperados
* Consistência da listagem
* Funcionamento da exclusão

Foram utilizados cenários baseados em:

* Fluxos positivos
* Fluxos negativos
* Validação de dados
* Testes exploratórios

---

# 6. Casos de teste

Os cenários e casos de teste foram documentados em uma planilha contendo:

* Identificação do teste
* Cenário
* Passos para execução
* Resultado esperado
* Resultado obtido
* Status do teste
* Evidência

Link da planilha:

COLOCAR LINK DO GOOGLE SHEETS AQUI

---

# 7. Execução dos testes

Os testes foram executados diretamente na aplicação disponibilizada no desafio.

Durante a execução foram coletadas evidências através de:

* prints de tela
* gravações curtas demonstrando os comportamentos observados

Link das evidências:

COLOCAR LINK DO DRIVE AQUI

---

# 8. Bugs identificados

## Bug 1 — Cadastro permitido com campos vazios

**Descrição**

O sistema permite cadastrar um curso sem preencher os campos do formulário.

**Passos para reproduzir**

1. Acessar a tela de cadastro
2. Deixar os campos sem preenchimento
3. Clicar em "Cadastrar curso"

**Resultado atual**

O sistema realiza o cadastro mesmo sem dados preenchidos.

**Resultado esperado**

O sistema deve impedir o cadastro e exibir mensagens de validação indicando campos obrigatórios.

**Severidade**

Alta

---

## Bug 2 — Data final anterior à data inicial

**Descrição**

O sistema permite cadastrar um curso com data de término anterior à data de início.

**Passos para reproduzir**

1. Acessar a tela de cadastro
2. Informar data de início posterior à data de fim
3. Realizar o cadastro

**Resultado atual**

O sistema aceita o cadastro mesmo com datas inconsistentes.

**Resultado esperado**

O sistema deve impedir o cadastro e informar que a data final não pode ser anterior à data inicial.

**Severidade**

Alta

---

## Bug 3 — Exclusão não remove curso da listagem

**Descrição**

Ao clicar para excluir um curso, o sistema apresenta mensagem de sucesso, porém o curso permanece visível na listagem.

**Passos para reproduzir**

1. Acessar a tela de listagem de cursos
2. Selecionar um curso
3. Clicar em "Excluir curso"

**Resultado atual**

A aplicação exibe mensagem de exclusão, mas o curso continua na listagem.

**Resultado esperado**

O curso deve ser removido da listagem após a exclusão.

**Severidade**

Alta

---

## Bug 4 — Problemas de responsividade na listagem

**Descrição**

A interface da listagem apresenta problemas de layout em resoluções menores.

**Resultado atual**

Os cards e elementos da interface não se ajustam corretamente em telas menores.

**Resultado esperado**

A interface deve se adaptar corretamente a diferentes resoluções.

**Severidade**

Média

---

# 9. Observações e melhorias

Durante a análise também foram identificadas algumas oportunidades de melhoria:

* Ausência de validação mínima nos campos
* Falta de limite de caracteres em campos de texto
* Possível padronização de formatação de entrada de dados

Esses pontos não impedem o funcionamento da aplicação, mas podem melhorar a qualidade e consistência dos dados.

---

# 10. Conclusão

A aplicação apresenta um fluxo simples e funcional, porém foram identificadas falhas importantes relacionadas à validação de dados e consistência das ações realizadas.

Os testes realizados buscaram cobrir os principais fluxos do sistema, explorando tanto cenários positivos quanto negativos, com foco na identificação de comportamentos inesperados e possíveis melhorias na qualidade da aplicação.
