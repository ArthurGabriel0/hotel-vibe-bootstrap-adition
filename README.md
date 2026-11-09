# 🏨 HotelVibe — Evolução com Bootstrap 5

**HotelVibe** é um projeto acadêmico de desenvolvimento web que simula a apresentação de um hotel e seu processo de reserva de hospedagem. A aplicação foi desenvolvida utilizando Vue.js 3 e, nesta etapa, recebeu uma evolução visual com a integração do framework CSS Bootstrap 5.

O objetivo desta atualização é aprimorar a interface, melhorar a responsividade e facilitar a organização dos elementos visuais, preservando a estrutura de componentes e a reatividade já existentes no Vue.js.

---

## 📌 Sobre o projeto

O HotelVibe apresenta uma interface de hotel fictício, permitindo que o usuário conheça as opções de acomodação, consulte avaliações demonstrativas e simule uma reserva.

Na evolução do projeto, foi integrado o Bootstrap 5 para aprimorar a construção dos elementos visuais e a adaptação da interface a diferentes tamanhos de tela.

## ✨ Funcionalidades

- Apresentação do hotel e de seus diferenciais.
- Exibição de quartos com imagens, descrições, capacidade e preços.
- Seleção de quartos para iniciar uma reserva.
- Formulário interativo com validação de informações.
- Seleção das datas de check-in e check-out.
- Seleção da quantidade de hóspedes.
- Cálculo automático do valor total conforme a quantidade de diárias.
- Exibição da confirmação e do resumo da reserva.
- Seção de avaliações demonstrativas de hóspedes.
- Navegação responsiva para dispositivos móveis e computadores.

> **Observação:** o sistema de reservas é demonstrativo. Não há integração com banco de dados, processamento de pagamentos ou armazenamento permanente das informações.

---

## 🛠️ Tecnologias utilizadas

| Tecnologia | Aplicação no projeto |
|---|---|
| Vue.js 3 | Construção da interface e dos componentes |
| JavaScript | Lógica e interatividade |
| HTML5 | Estrutura da aplicação |
| CSS3 | Estilização personalizada |
| Bootstrap 5 | Layout, componentes e responsividade |
| Vite | Ambiente de desenvolvimento e compilação |
| StackBlitz | Ambiente de desenvolvimento online |
| GitHub | Versionamento e hospedagem do código |

---

## 🎨 Melhorias implementadas com Bootstrap 5

A integração do Bootstrap 5 foi realizada para aprimorar a interface sem substituir a arquitetura Vue.js do projeto.

As principais melhorias foram:

1. **Cabeçalho responsivo:** implementação de uma navbar com menu recolhível em dispositivos menores.
2. **Cards de quartos:** utilização de classes Bootstrap para organizar os cartões, padronizar espaçamentos e aplicar sombras.
3. **Formulário de reserva:** aplicação de estilos padronizados nos campos, seletores, botões e mensagens de validação.
4. **Organização em colunas:** utilização do sistema de grid para distribuir quartos e avaliações de acordo com o tamanho da tela.
5. **Responsividade:** aplicação de classes como `col-12`, `col-md-6` e `col-lg-4`, permitindo diferentes distribuições em celulares, tablets e computadores.
6. **Elementos visuais:** utilização de classes como `shadow-sm`, `rounded-4`, `img-fluid`, `d-flex` e `gap-3`.

A identidade visual original foi preservada, mantendo a paleta de cores em tons de verde, bege e dourado, juntamente com a estilização personalizada em CSS.

---

## 🧩 Organização dos componentes

O projeto utiliza componentes Vue.js para dividir a interface em partes independentes e reutilizáveis.

| Arquivo | Responsabilidade |
|---|---|
| `App.vue` | Componente principal, responsável pela integração e pelo gerenciamento dos dados da aplicação. |
| `Header.vue` | Cabeçalho e navegação responsiva. |
| `QuartoCard.vue` | Exibição das informações e opções de reserva dos quartos. |
| `ReservaForm.vue` | Formulário, validação dos dados e cálculo da reserva. |
| `ReservaConfirmacao.vue` | Exibição da confirmação e do resumo da reserva. |
| `AvaliacaoCard.vue` | Apresentação das avaliações dos hóspedes. |

---

## 📚 Conceitos de Vue.js aplicados

Durante o desenvolvimento, foram utilizados conceitos fundamentais do Vue.js 3:

- **Componentes:** divisão da interface em partes reutilizáveis.
- **`<script setup>`:** organização da lógica dos componentes.
- **`ref()`:** criação e gerenciamento de dados reativos.
- **`v-for`:** renderização dinâmica de quartos e avaliações.
- **`v-if`:** exibição condicional de elementos.
- **`v-model`:** sincronização dos campos do formulário com os dados.
- **Props:** comunicação e passagem de dados entre componentes.
- **Eventos (`emit`):** comunicação entre componentes por meio de eventos personalizados.

---

## ▶️ Como executar o projeto

Para executar o projeto localmente, é necessário ter o Node.js instalado.

1. Clone o repositório:

   ```bash
   git clone https://github.com/ArthurGabriel0/hotel-vibe-bootstrap-adition.git
   ```

2. Entre na pasta do projeto:

   ```bash
   cd hotel-vibe-bootstrap-adition
   ```

3. Instale as dependências:

   ```bash
   npm install
   ```

4. Inicie o ambiente de desenvolvimento:

   ```bash
   npm run dev
   ```

5. Acesse o endereço local apresentado no terminal.

Para gerar a versão de produção:

```bash
npm run build
```

---

## 🤖 Utilização de inteligência artificial

A inteligência artificial foi utilizada como ferramenta de apoio durante o desenvolvimento do projeto, auxiliando no planejamento, na organização dos componentes, na implementação de melhorias visuais, na integração do Bootstrap 5 e na revisão da documentação.

Seu uso teve caráter complementar, sendo necessário que os integrantes revisem, compreendam e sejam capazes de explicar os códigos e as funcionalidades implementadas.

---

## 👥 Integrantes

- Arthur Gabriel — 04209021
- Letícia Alves — 04207296
- Pedro Maia — 04212837
- Kaio Ruan Felipe Lisboa — 04209555
- Vitor Angelo — 04211319

---

## 🎓 Objetivo acadêmico

Aplicar e aprofundar conhecimentos em desenvolvimento front-end por meio da evolução de uma aplicação Vue.js já existente, integrando o framework CSS Bootstrap 5.

A atividade busca demonstrar como um framework CSS pode contribuir para a organização visual, a padronização dos componentes e a responsividade de uma aplicação, mantendo os conceitos de componentização e reatividade do Vue.js.

---

**Projeto desenvolvido para fins acadêmicos.**

**HotelVibe — Conforto, elegância e boas experiências.**
