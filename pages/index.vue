<template>
  <div class="container">
    <nav class="navbar is-fixed-top" role="navigation" aria-label="main navigation">
      <div class="navbar-brand">
        <a class="navbar-item" href="https://bulma.io">
          <img src="https://bulma.io/images/bulma-logo.png" width="112" height="28">
        </a>

        <a role="button" class="navbar-burger burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample"
          :class="{ 'is-active': burgerActive }"
          @click="toggleBurger"
        >
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>

      <div id="navbarBasicExample" class="navbar-menu"
        :class="{ 'is-active': burgerActive }"
      >
        <div class="navbar-start">
          <a class="navbar-item">
            トップ
          </a>

          <a class="navbar-item">
            ご利用ガード
          </a>

          <div class="navbar-item has-dropdown is-hoverable">
            <a class="navbar-link">
              その他
            </a>
            <div class="navbar-dropdown">
              <a class="navbar-item">
                プライバシー
              </a>
              <a class="navbar-item">
                利用規約
              </a>
              <hr class="navbar-divider">
              <a class="navbar-item">
                問い合わせ
              </a>
              <a class="navbar-item">
                アンケート
              </a>
            </div>
          </div>
        </div>

        <div class="navbar-end">
          <div class="navbar-item">
            <div class="buttons">
              <a class="button is-primary">
                <strong>Sign up</strong>
              </a>
              <a class="button is-light">
                Log in
              </a>
            </div>
          </div>
        </div>
      </div>
    </nav>

    <section class="section">
      <div class="tabs is-toggle is-fullwidth">
        <ul>
          <li class="is-active">
            <a>
              <span>運行情報</span>
            </a>
          </li>
          <li>
            <a>
              <span>バス停地図</span>
            </a>
          </li>
          <li>
            <a>
              <span>時刻表</span>
            </a>
          </li>
        </ul>
      </div>
    </section>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  head: {
    bodyAttrs: {
      class: 'has-navbar-fixed-top'
    },
  },

  components: {
    Logo
  },

  data() {
    return {
      burgerActive: false,
    }
  },

  methods: {
    toggleBurger () {
      this.burgerActive = !this.burgerActive
    },
  },
}
</script>

<style>
/* .container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
} */
</style>
