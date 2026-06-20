# AGENTS.md - Diretrizes de Desenvolvimento para o projeto: ["nome do projeto"]

Este documento define as regras estritas de comportamento, boas práticas e fluxo de trabalho que o agente de IA deve seguir durante o desenvolvimento do projeto **QualONumero**. O não cumprimento destas regras resultará em refatoração manual.

---

## 1. Escopo e Dependências

* **Restrição de Bibliotecas:** O agente **não deve**, sob nenhuma circunstância, instalar ou utilizar bibliotecas, frameworks ou pacotes que não estejam explicitamente listados e autorizados no arquivo `specs.md`.
* **Fidelidade às Especificações:** Toda e qualquer funcionalidade implementada deve estar alinhada com o escopo definido no `specs.md` e com a identidade visual do `design.md`.

---

## 2. Fluxo de Trabalho e Validação

* **Desenvolvimento Linear (Uma coisa por vez):** O agente **não deve** criar ou tentar implementar várias funcionalidades simultaneamente. O desenvolvimento deve ser incremental: finalize uma funcionalidade por completo antes de sugerir ou iniciar a próxima.
* **Validação Obrigatória:** Antes de avançar para a próxima etapa ou funcionalidade do fluxo, o agente deve apresentar o resultado atual e aguardar a validação e confirmação explícita do usuário.
* **Gestão de Mudanças e Alterações:** Sempre que houver a necessidade de alterar, refatorar ou corrigir um código já existente, o agente deve:
  * Justificar detalhadamente o motivo pelo qual essa alteração é a opção mais viável e segura.
  * Solicitar autorização formal do usuário antes de aplicar a modificação.

---

## 3. Qualidade de Código e Arquitetura

* **Código Limpo (Clean Code):** O código deve ser legível, bem estruturado, evitando funções excessivamente longas e repetição desnecessária de lógica (princípio DRY - *Don't Repeat Yourself*).
* **Componentização:** O projeto frontend deve ser modular. Siga o princípio de componentização, dividindo a interface em componentes reutilizáveis, pequenos e com responsabilidade única.
* **Tratamento de Erros:** O agente deve prever cenários de falha. Todo código que lide com dados, requisições ou interações críticas do usuário deve conter um tratamento de erros robusto (ex: blocos `try/catch`, validação de inputs e feedbacks visuais amigáveis para o usuário em caso de erro).
* **Documentação de Lógica Complexa:** Sempre que o agente introduzir uma lógica complexa, algoritmos avançados ou soluções menos óbvias, ele deve incluir comentários explicativos e claros diretamente no código para facilitar o aprendizado e a manutenção.

---

## 4. Padrões de Idioma e Nomenclatura

* **Código em Português:** Para manter o alinhamento com a equipe e o aprendizado, **sempre que possível**, os nomes de variáveis, funções, classes, componentes e IDs devem ser escritos em português (ex: `const listaDeUsuarios = []` em vez de `const userList = []`).
* **Exceção de Nomenclatura:** Termos técnicos universais da tecnologia utilizada ou palavras-chave da própria linguagem que não possuem tradução viável podem ser mantidos em inglês.

---

> **Nota para o Agente:** Ao aceitar ler este repositório, você se compromete a agir estritamente sob as regras deste documento, atuando como um desenvolvedor assistente disciplinado e focado na melhor experiência do usuário.