

<script setup>
import { ref } from 'vue'

const props = defineProps({
  quartoSelecionado: Object
})

const emit = defineEmits(['confirmar'])

const nome = ref('')
const entrada = ref('')
const saida = ref('')
const hospedes = ref(1)
const erro = ref('')

function enviarReserva() {
  erro.value = ''

  if (!nome.value.trim() || !entrada.value || !saida.value) {
    erro.value = 'Preencha todos os campos.'
    return
  }

  if (saida.value <= entrada.value) {
    erro.value = 'A saída deve ser depois da entrada.'
    return
  }

  if (!props.quartoSelecionado) {
    erro.value = 'Selecione um quarto antes de reservar.'
    return
  }

  const inicio = new Date(entrada.value + 'T12:00:00')
  const fim = new Date(saida.value + 'T12:00:00')

  const diarias = Math.round((fim - inicio) / 86400000)

  emit('confirmar', {
    nome: nome.value,
    entrada: entrada.value,
    saida: saida.value,
    hospedes: hospedes.value,
    quarto: props.quartoSelecionado.nome,
    preco: props.quartoSelecionado.preco,
    diarias: diarias,
    total: diarias * props.quartoSelecionado.preco
  })
}
</script>

<template>
  <form
    class="card formulario border-0 shadow-sm"
    @submit.prevent="enviarReserva"
  >

    <div class="card-body p-4 p-md-5">

      <h3 class="titulo-formulario mb-4">
        Dados da reserva
      </h3>

      <!-- NOME -->
      <div class="mb-3">
        <label for="nome" class="form-label">
          Nome completo
        </label>

        <input
          id="nome"
          v-model="nome"
          type="text"
          class="form-control"
          placeholder="Digite seu nome"
        >
      </div>

      <!-- QUARTO -->
      <div class="mb-3">
        <label for="quarto" class="form-label">
          Quarto escolhido
        </label>

        <input
          id="quarto"
          :value="quartoSelecionado ? quartoSelecionado.nome : 'Selecione um quarto acima'"
          type="text"
          class="form-control"
          readonly
        >
      </div>

      <!-- DATAS -->
      <div class="row g-3 mb-3">

        <div class="col-12 col-md-6">
          <label for="entrada" class="form-label">
            Check-in
          </label>

          <input
            id="entrada"
            v-model="entrada"
            type="date"
            class="form-control"
          >
        </div>

        <div class="col-12 col-md-6">
          <label for="saida" class="form-label">
            Check-out
          </label>

          <input
            id="saida"
            v-model="saida"
            type="date"
            class="form-control"
            :min="entrada || undefined"
          >
        </div>

      </div>

      <!-- HÓSPEDES -->
      <div class="mb-3">
        <label for="hospedes" class="form-label">
          Quantidade de hóspedes
        </label>

        <select
          id="hospedes"
          v-model="hospedes"
          class="form-select"
        >
          <option :value="1">1 hóspede</option>
          <option :value="2">2 hóspedes</option>
          <option :value="3">3 hóspedes</option>
          <option :value="4">4 hóspedes</option>
        </select>
      </div>

      <!-- ERRO -->
      <div
        v-if="erro"
        class="alert alert-danger mt-3"
        role="alert"
      >
        {{ erro }}
      </div>

      <!-- BOTÃO -->
      <button
        type="submit"
        class="btn btn-confirmar w-100 mt-3"
      >
        Confirmar reserva
      </button>

    </div>
  </form>
</template>

<style scoped>
.formulario {
  background: white;
  border-radius: 12px;
}

.titulo-formulario {
  color: #102b26;
  font-family: 'Playfair Display', Georgia, serif;
  font-size: 25px;
}

.form-label {
  font-size: 13px;
  font-weight: bold;
  color: #102b26;
}

.form-control,
.form-select {
  padding: 12px;
  border: 1px solid #ddd;
  border-radius: 7px;
  font-family: 'DM Sans', Arial, sans-serif;
  font-size: 14px;
}

.form-control:focus,
.form-select:focus {
  border-color: #a17c3e;
  box-shadow: 0 0 0 0.2rem #d9b87940;
}

.btn-confirmar {
  padding: 14px;
  border: none;
  border-radius: 7px;
  background: #102b26;
  color: white;
  font-weight: bold;
  transition: 0.2s;
}

.btn-confirmar:hover {
  background: #244a40;
  color: white;
}

.alert {
  font-size: 13px;
  margin-bottom: 0;
}
</style>
