<template>
  <div id="wrapper">
    <nav class="navbar is-dark">
      <div class="navbar-brand">
        <router-link to="/" class="navbar-item">
          <strong> Loja Virtual Djackets Manaus </strong></router-link
        >
        <a
          class="navbar-burguer"
          aria-label="menu"
          aria-expanded="false"
          data-target="navbar-menu"
          @click="showMobileMenu = !showMobileMenu"
        >
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>
      <div class="navbar-menu" id="navbar-menu" v-bind:class="{ 'is-active': showMobileMenu}">
        <div class="navbar-end">
          <router-link to="/produtos" class="navbar-item">Produtos</router-link>
          <router-link to="/categorias" class="navbar-item">Categorias</router-link>

          <div class="navbar-item">
            <div class="buttons">
              <router-link to="/login" class="button is-light">Log in</router-link>

              <router-link to="/cart" class="button is-success">
                <span class="icon"><i class="fa-solid fa-cart-shopping"></i></span>
                <span>Carrinho</span>
              </router-link>
            </div>
          </div>
        </div>
      </div>
    </nav>

    <section class="section">
      <router-view />
    </section>
    
    <footer class="footer">
      <p class="has-text-centered">Todos os Direitos Reservados a Jean A. Silva 2022</p>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showMobileMenu: false,
    }
  }
}
</script>

<style lang="scss">
@import "../node_modules/bulma";
</style>
