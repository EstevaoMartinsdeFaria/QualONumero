# design.md - Guia de Estilo Visual: QualONumero

Este documento estabelece as diretrizes de design, paleta de cores, tipografia e animações para o jogo **QualONumero**. O objetivo é criar uma interface minimalista, amigável, com cores calmas e feedbacks visuais claros.

---

## 1. Paleta de Cores e Atmosfera

A identidade visual deve evitar cores excessivamente vibrantes ou saturadas, priorizando tons pastéis e opacos que transmitam tranquilidade e foco.

* **Fundo da Aplicação (Background):** Tom neutro e suave (ex: Cinza-azulado claro `#F4F6F9` ou Creme suave `#FDFBF7`).
* **Cor Principal (Elementos de Destaque):** Azul calmo ou Verde sálvia (ex: Azul soft `#5A7D9A` ou Verde sálvia `#7A9A82`) para botões e links importantes.
* **Cor de Alerta/Aviso:** Um tom de terracota ou vermelho queimado (ex: `#C96F6F`) para indicar erros de forma visível, mas sem agressividade visual.
* **Textos:** Grafite escuro (`#2C3E50`) para garantir excelente contraste e leitura.

---

## 2. Tipografia e Hierarquia de Texto

* **Fonte Recomendada:** Uma fonte *Sans-serif* moderna e limpa, como **Inter**, **Roboto** ou **Poppins** (disponíveis no Google Fonts).
* **Títulos (Nome do jogo e Widgets):** Devem ser grandes, em negrito (`font-weight: 700`) e centralizados.
* **Textos de Boas-Vindas e Instruções:** Tamanho médio (`1.2rem` ou `18px`), com espaçamento extra para facilitar a leitura.
* **Textos de Aviso (Maior/Menor):** **Grandes e destacados**. Devem usar uma variação de peso em negrito para capturar a atenção do jogador imediatamente após o palpite.

---

## 3. Componentes e Elementos de UI

* **Botões ("Novo Jogo" / "Tentar Novamente"):**
* Devem ser **altamente destacados** na tela.
* Use a Cor Principal com preenchimento sólido e cantos suavemente arredondados (`border-radius: 8px`).
* Adicione um leve efeito de sombra (*box-shadow*) e mudança sutil de cor ao passar o mouse (*hover*) para indicar interatividade.


* **Campo de Entrada (Input):**
* Centralizado, com tamanho de fonte grande para o número digitado.
* Borda simples e elegante que muda de cor quando o campo ganha foco.



---

## 4. Animações e Microinterações (Crucial)

As interações visuais guiarão a experiência do usuário sem a necessidade de textos longos.

### 4.1. Alerta de Valor Inválido

Quando o jogador tentar inserir um caractere que não seja um número inteiro entre 1 e 100 (letras, símbolos ou números fora do escopo), o sistema deve acionar o seguinte comportamento visual:

1. **Animação de Tremor (Shake):** O campo de inserção numérico deve balançar/tremer horizontalmente de forma rápida, simulando um movimento de "não".
2. **Texto Piscante:** Uma etiqueta em caixa alta com o texto **"VALOR INVÁLIDO"** deve aparecer logo acima do campo de entrada, piscando em vermelho queimado por 1.5 segundos antes de sumir.

### 4.2. Transições de Widgets (Vitória e Derrota)

* Os componentes de estilo *widget* (modais de fim de jogo) não devem aparecer abruptamente na tela.
* Devem utilizar uma **animação suave de surgimento** (efeito *Fade-In* combinado com um leve *Slide-Up*, onde o widget desliza suavemente de baixo para cima enquanto ganha opacidade).
* O fundo atrás do widget deve ganhar uma camada de desfoque suave (*backdrop-blur*) ou escurecimento parcial para isolar a atenção do jogador no resultado.