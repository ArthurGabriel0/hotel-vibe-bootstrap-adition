

<script setup>
import { ref } from 'vue'

import Header from './components/Header.vue'
import QuartoCard from './components/QuartoCard.vue'
import ReservaForm from './components/ReservaForm.vue'
import AvaliacaoCard from './components/AvaliacaoCard.vue'
import ReservaConfirmacao from './components/ReservaConfirmacao.vue'

const quartoSelecionado = ref(null)
const reserva = ref(null)

const quartos = [
  {
    id: 1,
    nome: 'Quarto Standard',
    categoria: 'Conforto essencial',
    descricao: 'Um ambiente aconchegante para descansar e aproveitar sua viagem.',
    preco: 180,
    hospedes: 2,
    imagem: 'https://images.unsplash.com/photo-1611892440504-42a792e24d32?auto=format&fit=crop&w=800&q=80'
  },
  {
    id: 2,
    nome: 'Quarto Deluxe',
    categoria: 'Mais conforto',
    descricao: 'Mais espaço, elegância e conforto para uma estadia especial.',
    preco: 280,
    hospedes: 3,
    imagem: 'https://images.unsplash.com/photo-1590490360182-c33d57733427?auto=format&fit=crop&w=800&q=80'
  },
  {
    id: 3,
    nome: 'Suíte Premium',
    categoria: 'Experiência exclusiva',
    descricao: 'Uma suíte sofisticada para quem deseja uma experiência diferenciada.',
    preco: 450,
    hospedes: 4,
    imagem: 'https://images.unsplash.com/photo-1582719478250-c89cae4dc85b?auto=format&fit=crop&w=800&q=80'
  }
]

const avaliacoes = [
  {
    id: 1,
    nome: 'Mariana Costa',
    comentario: 'Ambiente maravilhoso, quarto confortável e atendimento excelente!'
  },
  {
    id: 2,
    nome: 'Pedro Almeida',
    comentario: 'Tudo muito organizado. Foi uma experiência tranquila e especial.'
  },
  {
    id: 3,
    nome: 'Camila Santos',
    comentario: 'Adorei o conforto e a decoração. Voltaria com certeza!'
  }
]

function selecionarQuarto(quarto) {
  quartoSelecionado.value = quarto
  reserva.value = null

  document.getElementById('reservar').scrollIntoView({
    behavior: 'smooth'
  })
}

function confirmarReserva(dados) {
  reserva.value = dados
}
</script>

<template>
  <Header />

  <main>
    <!-- HERO -->
    <section id="inicio" class="hero">
      <div class="hero-conteudo">
        <span class="subtitulo">SUA ESTADIA, NOSSO CUIDADO</span>

        <h1>Momentos especiais começam com uma boa estadia.</h1>

        <p>
          Conforto, elegância e hospitalidade em um só lugar.
          Encontre o quarto ideal para sua próxima viagem.
        </p>

        <a href="#quartos" class="botao-principal btn btn-dark shadow-sm">
          Explorar quartos →
        </a>

        <div class="destaques">
          <span>✓ Conforto e qualidade</span>
          <span>✓ Atendimento especial</span>
        </div>
      </div>

      <div class="hero-imagem rounded-4 shadow-sm">
        <img
          class="img-fluid"
          src="https://images.unsplash.com/photo-1566073771259-6a8506099945?auto=format&fit=crop&w=1200&q=85"
          alt="Hotel elegante com piscina"
        >

        <div class="selo shadow-sm">
          <strong>HotelVibe</strong>
          <span>Sua experiência começa aqui</span>
        </div>
      </div>
    </section>

    <!-- BENEFÍCIOS -->
    <section class="beneficios container-fluid">
      <div>
        <span class="beneficio-icone">✧</span>
        <div>
          <strong>Conforto garantido</strong>
          <p>Ambientes pensados para você.</p>
        </div>
      </div>

      <div>
        <span class="beneficio-icone">⌂</span>
        <div>
          <strong>Espaços acolhedores</strong>
          <p>Seu descanso é nossa prioridade.</p>
        </div>
      </div>

      <div>
        <span class="beneficio-icone">♡</span>
        <div>
          <strong>Atendimento especial</strong>
          <p>Cuidado em cada detalhe.</p>
        </div>
      </div>
    </section>

    <!-- QUARTOS -->
    <section id="quartos" class="secao container-fluid">
      <div class="titulo-secao">
        <span class="subtitulo">ENCONTRE SEU ESPAÇO</span>
        <h2>Quartos pensados para você</h2>
        <p>Escolha a acomodação ideal para sua próxima experiência.</p>
      </div>

      <div class="row g-4">
        <div
          v-for="quarto in quartos"
          :key="quarto.id"
          class="col-12 col-md-6 col-lg-4"
        >
          <QuartoCard
            :quarto="quarto"
            @reservar="selecionarQuarto"
          />
        </div>
      </div>
    </section>

    <!-- RESERVAS -->
    <section id="reservar" class="secao secao-reserva container-fluid">
      <div class="titulo-secao">
        <span class="subtitulo">FAÇA SUA ESCOLHA</span>
        <h2>Reserve sua estadia</h2>
        <p>Preencha seus dados para simular uma reserva.</p>
      </div>

      <div class="reserva-layout">
        <div class="reserva-info">
          <h3>Sua próxima experiência está mais perto.</h3>

          <p>
            Escolha seu quarto, informe as datas e veja o resumo
            da sua hospedagem.
          </p>

          <div v-if="quartoSelecionado" class="quarto-escolhido shadow-sm">
            <span>QUARTO SELECIONADO</span>

            <h3>{{ quartoSelecionado.nome }}</h3>

            <p>
              R$ {{ quartoSelecionado.preco.toFixed(2).replace('.', ',') }}
              por diária
            </p>
          </div>

          <div v-else class="aviso-quarto shadow-sm">
            Selecione um dos quartos acima para começar sua reserva.
          </div>
        </div>

        <div>
          <ReservaForm
            :quartoSelecionado="quartoSelecionado"
            @confirmar="confirmarReserva"
          />

          <ReservaConfirmacao :reserva="reserva" />
        </div>
      </div>
    </section>

    <!-- AVALIAÇÕES -->
    <section id="avaliacoes" class="secao avaliacoes-secao container-fluid">
      <div class="titulo-secao">
        <span class="subtitulo">EXPERIÊNCIAS QUE INSPIRAM</span>
        <h2>O que dizem nossos hóspedes</h2>
        <p>Avaliações demonstrativas da experiência HotelVibe.</p>
      </div>

      <div class="row g-4">
        <div
          v-for="avaliacao in avaliacoes"
          :key="avaliacao.id"
          class="col-12 col-md-6 col-lg-4"
        >
          <AvaliacaoCard :avaliacao="avaliacao" />
        </div>
      </div>
    </section>
  </main>

  <!-- RODAPÉ -->
  <footer class="footer">
    <a href="#inicio" class="logo-footer">
      Hotel<span>Vibe</span>
    </a>

    <p>Conforto, elegância e boas experiências.</p>

    <small>Projeto acadêmico desenvolvido em Vue.js.</small>
  </footer>
</template>
