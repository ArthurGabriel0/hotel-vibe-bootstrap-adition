

<script setup>
defineProps({
  quarto: Object
})

defineEmits(['reservar'])
</script>

<template>
  <article class="card quarto-card h-100 border-0 shadow-sm">

    <img
      :src="quarto.imagem"
      :alt="quarto.nome"
      class="card-img-top imagem-quarto"
    >

    <div class="card-body d-flex flex-column p-4">

      <span class="badge categoria align-self-start mb-3">
        {{ quarto.categoria }}
      </span>

      <h3 class="card-title titulo-quarto">
        {{ quarto.nome }}
      </h3>

      <p class="card-text descricao">
        {{ quarto.descricao }}
      </p>

      <div class="detalhes d-flex flex-wrap gap-2 mb-4">
        <span class="badge detalhe-badge">
          ♙ {{ quarto.hospedes }} hóspedes
        </span>

        <span class="badge detalhe-badge">
          Wi-Fi grátis
        </span>
      </div>

      <div class="rodape-quarto mt-auto">

        <div>
          <strong class="preco">
            R$ {{ quarto.preco }}
          </strong>

          <small class="text-secondary">/ diária</small>
        </div>

        <button
          class="btn btn-reservar"
          @click="$emit('reservar', quarto)"
        >
          Reservar
        </button>

      </div>

    </div>
  </article>
</template>

<style scoped>
.quarto-card {
  border-radius: 12px;
  overflow: hidden;
  background: white;
  transition: transform 0.25s, box-shadow 0.25s;
}

.quarto-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 12px 30px #102b2620 !important;
}

.imagem-quarto {
  width: 100%;
  height: 210px;
  object-fit: cover;
}

.categoria {
  background: #f1ebdc;
  color: #96713a;
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 1px;
  padding: 8px 11px;
}

.titulo-quarto {
  color: #102b26;
  font-family: 'Playfair Display', Georgia, serif;
  font-size: 22px;
  margin-bottom: 12px;
}

.descricao {
  color: #777;
  line-height: 1.7;
  font-size: 14px;
  min-height: 45px;
}

.detalhe-badge {
  background: #f5f3eb;
  color: #536158;
  font-weight: 500;
  padding: 8px 10px;
  font-size: 11px;
}

.rodape-quarto {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 10px;
  border-top: 1px solid #eee;
  padding-top: 18px;
}

.preco {
  color: #102b26;
  font-size: 22px;
}

.btn-reservar {
  background: #102b26;
  color: white;
  border: none;
  border-radius: 6px;
  padding: 11px 16px;
  font-size: 13px;
  font-weight: 600;
  transition: 0.2s;
}

.btn-reservar:hover {
  background: #244a40;
  color: white;
}

@media (max-width: 400px) {
  .rodape-quarto {
    align-items: flex-start;
    flex-direction: column;
  }
}
</style>
