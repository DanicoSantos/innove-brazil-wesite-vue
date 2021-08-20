<template>
  <div id="app" class="app">
    <div id="nav">
      <nav
        class="navbar is-dark"
        role="navigation"
        aria-label="main navigation"
      >
        <div class="container">
          <div class="navbar-brand">
            <a class="navbar-item" href="https://bulma.io">
              <img
                src="https://bulma.io/images/bulma-logo.png"
                width="112"
                height="28"
              />
            </a>

            <a
              role="button"
              class="navbar-burger"
              aria-label="menu"
              aria-expanded="false"
              data-target="navbarBasicExample"
            >
              <span aria-hidden="true"></span>
              <span aria-hidden="true"></span>
              <span aria-hidden="true"></span>
            </a>
          </div>

          <div id="navbarBasicExample" class="navbar-menu">
            <div class="navbar-end">
              <a class="navbar-item">
                Home
              </a>

              <a class="navbar-item">
                Sobre
              </a>

              <a class="navbar-item">
                Serviço
              </a>

              <a class="navbar-item">
                Parceiros
              </a>

              <a class="navbar-item">
                Contato
              </a>
            </div>
          </div>
        </div>
      </nav>
    </div>

    <!-- begin: Main content view -->
    <main>
      <router-view />
    </main>
    <!-- end: Main content view -->
    <!-- begin: Footer -->
    <footer class="footer is-info">
      <div class="container">
        <div class="columns">
          <div class="column">
            <div class="footer__contact">
              <address class="footer__address">
                <strong>Edifício Empresarial Bolonha</strong> <br />
                Av. José Malcher, 168, sala 110
              </address>
              <p class="footer__phone my-4">
                +55 (91) 98111-1762
              </p>
              <p class="footer__email">Bertram.heinze@innovbrazil.com</p>
            </div>
          </div>
          <div class="column">
            <img src="https://via.placeholder.com/200x80" alt="" />
          </div>
          <div class="column">
            <a href="/"
              ><span class="icon"><i class="fas fa-instagram"></i></span
            ></a>
            <a href="/"
              ><span class="icon"><i class="fas fa-facebook"></i></span
            ></a>
          </div>
        </div>
      </div>
    </footer>
    <!-- end: Footer -->
  </div>
</template>

<style lang="scss">
@import "../node_modules/bulma/";

.footer__contact {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100%;
}
</style>
