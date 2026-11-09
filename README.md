# HotelVibe 🏨

**Site de hospedagem desenvolvido com Vue.js**

## 📌 Sobre o projeto

O HotelVibe é um site de hotel desenvolvido como projeto acadêmico, com o objetivo de praticar os principais conceitos do framework Vue.js.

A aplicação apresenta opções de quartos, avaliações de hóspedes e um formulário interativo de reserva, permitindo selecionar um quarto, informar os dados da hospedagem e visualizar o valor total da estadia.

## ✨ Funcionalidades

- Apresentação do hotel e de seus diferenciais.
- Exibição de quartos com imagens, descrições, capacidade e preços.
- Seleção de quarto para realizar uma reserva.
- Formulário com validação de informações.
- Cálculo do valor total conforme a quantidade de diárias.
- Exibição da confirmação da reserva.
- Seção de avaliações de hóspedes.
- Layout responsivo para diferentes tamanhos de tela.

## 🛠️ Tecnologias utilizadas

- Vue.js 3
- JavaScript
- HTML5
- CSS3
- StackBlitz
- GitHub

## 🧩 Organização dos componentes

O projeto foi dividido em componentes para facilitar a organização, a manutenção e o reaproveitamento do código.

| Componente | Responsabilidade |
|---|---|
| `Header.vue` | Exibe o cabeçalho e a navegação do site. |
| `QuartoCard.vue` | Apresenta as informações de cada quarto. |
| `ReservaForm.vue` | Recebe e valida os dados da reserva. |
| `ReservaConfirmacao.vue` | Exibe os dados e o valor da reserva confirmada. |
| `AvaliacaoCard.vue` | Apresenta as avaliações dos hóspedes. |
| `App.vue` | Integra os componentes e controla os dados principais da aplicação. |

## 📚 Conceitos de Vue.js aplicados

- **Componentes:** divisão da interface em partes independentes e reutilizáveis.
- **`<script setup>`:** sintaxe utilizada nos componentes para organizar a lógica.
- **`ref()`:** criação de dados reativos.
- **`v-for`:** renderização de listas de quartos e avaliações.
- **`v-if`:** exibição condicional de elementos.
- **`v-model`:** ligação entre os campos do formulário e os dados.
- **Eventos:** execução de funções em resposta às interações do usuário.
- **Props:** passagem de dados de um componente para outro.
- **CSS:** estilização própria da aplicação.

## 🤖 Uso de inteligência artificial

A inteligência artificial foi utilizada como ferramenta de apoio ao desenvolvimento, auxiliando no planejamento da estrutura, na criação inicial dos componentes, na integração da aplicação, na estilização e na organização da documentação.

Os integrantes devem revisar os códigos e compreender as funcionalidades antes da apresentação.

### Registro dos prompts utilizados

Os itens abaixo resumem as solicitações feitas durante o desenvolvimento. Eles devem ser ajustados para corresponder às solicitações realmente utilizadas pela equipe.

| Etapa | Resumo da solicitação à IA |
|---|---|
| 1. Planejamento | Solicitação de ajuda para planejar a estrutura de um site de hotel antes de começar a programar. |
| 2. Estrutura do projeto | Definição da organização dos componentes e da criação do projeto no StackBlitz. |
| 3. Cabeçalho e quartos | Solicitação de código para o cabeçalho e para um componente reutilizável de apresentação dos quartos. |
| 4. Reservas | Solicitação dos componentes de formulário de reserva, confirmação e avaliação. |
| 5. Integração | Solicitação da integração dos componentes no `App.vue` e da criação do CSS geral. |
| 6. Testes e documentação | Apoio na verificação das funcionalidades e na preparação da documentação do projeto. |

**Importante:** a equipe deve conferir o histórico de conversas e adaptar esse registro, acrescentando ou corrigindo os prompts conforme necessário. A IA foi utilizada como apoio, e o funcionamento do projeto deve ser verificado pelos integrantes.

## ▶️ Como executar o projeto

1. Abra o projeto no StackBlitz.
2. Aguarde o carregamento das dependências.
3. Utilize a pré-visualização para acessar o HotelVibe.
4. Teste a seleção de quartos, o formulário e a confirmação da reserva.

## 👥 Integrantes

- Arthur Gabriel - 04209021
- Letícia Alves - 04207296
- Pedro Maia - 04212837
- Kaio Ruan Felipe Lisboa - 04209555
- Juliana de Souza Barros 04209576
- Vitor Angelo - 04211319


## 🎓 Objetivo acadêmico

Aplicar conceitos fundamentais de desenvolvimento web com Vue.js, incluindo componentes, reatividade, diretivas, eventos, propriedades, formulários e estilização.

---

Projeto desenvolvido para fins acadêmicos.