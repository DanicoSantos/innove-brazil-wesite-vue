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

    <!-- Main content view -->
    <main>
      <router-view />
    </main>
  </div>
</template>

<style lang="scss">
@import "../node_modules/bulma/";
</style>
