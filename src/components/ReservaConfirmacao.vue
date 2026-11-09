
<script setup>
defineProps({
  reserva: Object
})
</script>

<template>
  <div v-if="reserva" class="confirmacao">
    <div class="icone">✓</div>

    <h2>Reserva realizada!</h2>
    <p>Obrigado por escolher o HotelVibe, {{ reserva.nome }}.</p>

    <div class="resumo">
      <p><strong>Quarto:</strong> {{ reserva.quarto }}</p>
      <p><strong>Check-in:</strong> {{ reserva.entrada }}</p>
      <p><strong>Check-out:</strong> {{ reserva.saida }}</p>
      <p><strong>Hóspedes:</strong> {{ reserva.hospedes }}</p>
      <p><strong>Diárias:</strong> {{ reserva.diarias }}</p>
      <p class="total">
        Valor total: R$ {{ reserva.total.toFixed(2).replace('.', ',') }}
      </p>
    </div>

    <small>Esta é uma confirmação demonstrativa, sem pagamento real.</small>
  </div>
</template>

<style scoped>
.confirmacao {
  background: #edf6ef;
  border: 1px solid #c6e5ce;
  border-radius: 12px;
  padding: 28px;
  margin-top: 24px;
  color: #183d2b;
}

.icone {
  display: grid;
  place-items: center;
  width: 48px;
  height: 48px;
  border-radius: 50%;
  background: #246b43;
  color: white;
  font-size: 28px;
}

h2 {
  margin-bottom: 8px;
}

.resumo {
  background: white;
  border-radius: 8px;
  padding: 16px;
  margin: 20px 0;
}

.resumo p {
  margin: 10px 0;
}

.total {
  border-top: 1px solid #ddd;
  padding-top: 14px;
  font-size: 18px;
  font-weight: bold;
}

small {
  color: #55705d;
}
</style>
