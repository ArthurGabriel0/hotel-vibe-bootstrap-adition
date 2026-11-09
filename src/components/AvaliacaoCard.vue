

<script setup>
defineProps({
  avaliacao: Object
})
</script>

<template>
  <article class="card avaliacao-card h-100 border-0 shadow-sm">
    <div class="card-body p-4">

      <div class="estrelas mb-3">
        ★★★★★
      </div>

      <p class="comentario">
        “{{ avaliacao.comentario }}”
      </p>

      <div class="hospede d-flex align-items-center gap-3">

        <div class="avatar">
          {{ avaliacao.nome.charAt(0) }}
        </div>

        <div>
          <strong class="nome-hospede">
            {{ avaliacao.nome }}
          </strong>

          <p class="descricao-hospede mb-0">
            Hóspede do HotelVibe
          </p>
        </div>

      </div>

    </div>
  </article>
</template>

<style scoped>
.avaliacao-card {
  background: white;
  border-radius: 12px;
  transition: transform 0.25s, box-shadow 0.25s;
}

.avaliacao-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 12px 30px #102b2620 !important;
}

.estrelas {
  color: #bd9145;
  letter-spacing: 3px;
  font-size: 19px;
}

.comentario {
  color: #606a66;
  line-height: 1.8;
  min-height: 80px;
  font-size: 14px;
}

.hospede {
  border-top: 1px solid #eee;
  padding-top: 16px;
}

.avatar {
  display: grid;
  place-items: center;
  width: 44px;
  height: 44px;
  flex-shrink: 0;
  border-radius: 50%;
  background: #e8eee9;
  color: #102b26;
  font-weight: bold;
  font-size: 17px;
}

.nome-hospede {
  color: #102b26;
  font-size: 14px;
}

.descricao-hospede {
  margin-top: 5px;
  color: #888;
  font-size: 12px;
}
</style>
