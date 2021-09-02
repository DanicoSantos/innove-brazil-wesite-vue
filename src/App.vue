<template>
  <div id="app" class="app" v-on:scroll="changeNavbarOnScroll">
    <div id="nav">
      <nav
        class="navbar is-dark is-fixed-top"
        role="navigation"
        aria-label="main navigation"
      >
        <div class="container">
          <div class="navbar-brand">
            <a class="navbar-item" href="/">
              <img
                src="@/assets/img/innovbrazil-logo-pb.png"
                width="150"
                height="30"
                class=""
              />
              <img
                class="is-hidden"
                src="@/assets/img/innovbrazil-logo.png"
                width="150"
                height="30"
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
              <router-link to="/" class="navbar-item">
                Home
              </router-link>

              <router-link to="/about" class="navbar-item">
                Sobre
              </router-link>

              <router-link to="/services" class="navbar-item">
                Serviços
              </router-link>

              <router-link to="/partners" class="navbar-item">
                Parceiros
              </router-link>

              <a href="#contact" class="navbar-item">
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
    <footer class="footer">
      <div class="container">
        <div class="columns">
          <div class="column">
            <div class="footer__contact">
              <address class="footer__address">
                <strong class="has-text-white"
                  >Edifício Empresarial Bolonha</strong
                >
                <br />
                Av. José Malcher, 168, sala 110
              </address>
              <p class="footer__phone my-4">
                +55 (91) 98111-1762
              </p>
              <p class="footer__email">Bertram.heinze@innovbrazil.com</p>
            </div>
          </div>
          <div
            class="column has-text-centered is-flex is-align-items-center is-justify-content-center"
          >
            <figure>
              <img
                src="@/assets/img/innovbrazil-logo-pb.png"
                width="184"
                height="60"
                alt=""
              />
            </figure>
          </div>
          <div
            class="column is-flex is-align-items-center is-justify-content-flex-end"
          >
            <div
              class="is-flex is-justify-content-center is-align-items-center"
            >
              <a href="/">
                <img src="@/assets/img/icons/instagram.svg" width="31" alt="" />
              </a>
              <a href="/" class="mx-4">
                <img src="@/assets/img/icons/facebook.svg" width="28" alt="" />
              </a>
            </div>
          </div>
        </div>
      </div>
    </footer>
    <!-- end: Footer -->
  </div>
</template>

<style lang="scss">
@import "assets/scss/variables.scss";
@import "../node_modules/bulma/";

.footer {
  background-color: $primaryColor;
}

.footer__contact {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100%;
  color: #fff;
}

/* 
* Bulma reset 
*/

// Navbar
.navbar.is-dark {
  background-color: transparent;
}

.navbar {
  transition: 0.5s ease;
}

.navbar-item img {
  max-height: unset;
}

// Buttons
.button {
  border-radius: 0px;
}

.button.is-info {
  background-color: $primaryColor;
}
</style>
