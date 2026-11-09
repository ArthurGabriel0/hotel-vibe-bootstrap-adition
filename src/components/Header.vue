

<script setup>
</script>

<template>
  <header>
    <nav class="navbar navbar-expand-lg navbar-dark header">
      <div class="container-fluid px-4 px-lg-5">

        <a href="#inicio" class="navbar-brand logo">
          Hotel<span>Vibe</span>
        </a>

        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#menuHotel"
          aria-controls="menuHotel"
          aria-expanded="false"
          aria-label="Abrir menu"
        >
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="menuHotel">
          <ul class="navbar-nav mx-auto mb-3 mb-lg-0">
            <li class="nav-item">
              <a class="nav-link" href="#inicio">Início</a>
            </li>

            <li class="nav-item">
              <a class="nav-link" href="#quartos">Quartos</a>
            </li>

            <li class="nav-item">
              <a class="nav-link" href="#avaliacoes">Avaliações</a>
            </li>
          </ul>

          <a href="#reservar" class="btn btn-reservar">
            Reservar agora
          </a>
        </div>

      </div>
    </nav>
  </header>
</template>

<style scoped>
.header {
  background: #102b26;
  padding: 15px 0;
}

.logo {
  font-family: 'Playfair Display', Georgia, serif;
  font-size: 27px;
  font-weight: bold;
  color: white;
}

.logo span {
  color: #d9b879;
}

.nav-link {
  color: #f0f0f0 !important;
  font-size: 14px;
  margin: 0 10px;
  transition: color 0.2s;
}

.nav-link:hover {
  color: #d9b879 !important;
}

.btn-reservar {
  background: #d9b879;
  color: #102b26;
  font-size: 13px;
  font-weight: bold;
  padding: 11px 19px;
  border-radius: 7px;
  transition: 0.2s;
}

.btn-reservar:hover {
  background: #ebd29e;
  color: #102b26;
}

.navbar-toggler {
  border-color: #d9b879;
}

@media (max-width: 991px) {
  .navbar-collapse {
    padding: 20px 0 5px;
  }

  .nav-link {
    margin: 5px 0;
  }

  .btn-reservar {
    display: inline-block;
    margin-top: 8px;
  }
}
</style>
