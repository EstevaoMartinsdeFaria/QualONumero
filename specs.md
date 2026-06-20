# specs.md - Especificações do Projeto: QualONumero

Este documento descreve as funcionalidades, regras de negócio e arquitetura do jogo **QualONumero**. O objetivo principal é criar um jogo casual, rápido e de escopo simplificado para passar o tempo.

---

## 1. Visão Geral do Projeto

* **Nome do Jogo:** QualONumero
* **Proposta:** Jogo rápido de adivinhação de números.
* **Plataforma:** Web (Frontend)
* **Tecnologias Recomendadas:** HTML5, Tailwind CSS (para estilização rápida e moderna) e JavaScript Vanilla (sem necessidade de frameworks complexos para manter a leveza do app).

---

## 2. Fluxo de Telas e Interface

A aplicação deve ser uma *Single Page Application* (SPA), alternando os estados da tela dinamicamente.

### 2.1. Tela Inicial

* **Título:** Exibir em destaque o nome do jogo: `QualONumero`.
* **Texto de Boas-Vindas:** Um texto receptivo para o jogador.
* **Subtexto Obrigatório:** Abaixo das boas-vindas, deve constar exatamente a frase:
> "voce tem 1 em 100 de acerta a resposta correta!"


* **Ação:** Um botão centralizado com o texto `novo jogo` que inicia a partida.

### 2.2. Tela de Jogo (Partida Ativa)

* **Campo de Entrada (Input):** Um campo numérico para o jogador inserir um valor de 1 a 100.
* **Indicador de Tentativas:** Exibir claramente a quantidade de vidas/tentativas restantes (começando em 5).
* **Histórico:** Exibir uma lista ou linha com os "últimos chutes" já realizados pelo jogador na partida atual.
* **Feedback Dinâmico:** Caso o jogador erre o palpite, um texto explicativo deve aparecer logo abaixo do campo de entrada informando se o número sorteado é **maior** ou **menor** do que o número que ele acabou de digitar.

### 2.3. Tela de Vitória (Widget/Modal)

Uma sobreposição estilo *widget* na tela que surge imediatamente quando o jogador acerta o número.

* **Mensagem:** Texto parabenizando o jogador.
* **Informações:** Revelar o número sorteado e exibir em quantas tentativas o jogador conseguiu acertar.
* **Ação:** Botão com o texto `novo jogo` para reiniciar o ciclo.

### 2.4. Tela de Derrota (Widget/Modal)

Uma sobreposição estilo *widget* na tela que surge se as 5 tentativas forem esgotadas.

* **Mensagem:** Texto lamentando que o jogador perdeu.
* **Informações:** Revelar qual era o número sorteado correto.
* **Ação:** Botão com o texto `tentar novamente` que limpa o estado atual e reinicia o jogo.

---

## 3. Regras de Negócio e Lógica

* **Sorteio do Número:** Sempre que um novo jogo iniciar, o sistema deve gerar um número inteiro aleatório no intervalo fechado de 1 a 100.
* **Limite de Vidas:** O jogador inicia com exatamente 5 vidas. Cada chute incorreto consome 1 vida.
* **Validação de Entrada:** O campo de entrada não deve aceitar números menores que 1, maiores que 100, campos vazios ou letras e simbulos. Se o usuário digitar algo inválido, o sistema deve alertar sem consumir uma vida.
* **Persistência de Estado:** Não há necessidade de salvar o progresso em banco de dados ou LocalStorage, pois as partidas são independentes e rápidas.

---

## 4. Prioridades de Implementação

Para garantir o desenvolvimento ágil, o agente deve focar nas tarefas nesta ordem:

1. **Prioridade Alta (Core):** Lógica de geração do número aleatório, sistema de contagem de 5 vidas e validação do chute (maior/menor).
2. **Prioridade Média (Interface):** Estruturação da Tela Inicial e da Tela de Jogo com o histórico de palpites.
3. **Prioridade Baixa (Polimento):** Criação dos Widgets de feedback visual (Vitória/Derrota) e aplicação dos estilos visuais rápidos.