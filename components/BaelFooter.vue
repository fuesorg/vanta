<template>
  <footer class="fill-gray-lighter xs-text-6 md-text-5">
    <div class="r no-gap">
      <div v-if="pagination.active" class="c-12 xs-text-left xs-p2">
        <lazy-bael-pagination :pagination="pagination" />
      </div>
      <div
        class="xs-text-left xs-p2 xs-border xs-border-right-none xs-border-bottom-none"
        :class="signupAboutSize"
      >
        <div class="item">
          <div v-if="siteDescription" class="footer__heading xs-mb2">About</div>
          <p v-if="siteDescription">{{siteDescription}}</p>
        </div>
      </div>
      <div
        v-if="signupBoolean"
        class="c-25 xs-text-left xs-p2 xs-border xs-border-right-none xs-border-bottom-none"
      >
        <lazy-send-grid />
      </div>
      <div
        class="xs-text-left xs-p2 xs-border xs-border-right-none xs-border-bottom-none"
        :class="signupAboutSize"
      >
        <div class="item">
          <div v-if="connectData" class="footer__heading xs-mb2">Connect</div>
          <ul v-if="connectData" class="list-unstyled">
            <li v-for="(c,i) in connectData" :key="i">
              <a :href="c.url">{{c.name}}</a>
            </li>
          </ul>
        </div>
      </div>
      <div
        class="xs-text-left xs-p2 xs-border xs-border-right-none xs-border-bottom-none"
        :class="signupAboutSize"
      >
        <div class="item">
          <div class="footer__heading xs-mb2">Deploy</div>

          <a
            href="https://vercel.com/new/git/external?repository-url=https%3A%2F%2Fgithub.com%2Fvercel%2Fnext.js%2Ftree%2Fcanary%2Fexamples%2Fhello-world"
          >
            <img
              style="height:24px;width:auto;"
              src="https://vercel.com/button"
              title="Deploy with Vercel"
            />
          </a>
        </div>
      </div>
      <div class="c-12 xs-text-left xs-p2 xs-border xs-border-right-none xs-border-bottom-none">
        <div class="item xs-text-6">
          © 2020 <a href="https://github.com/fuesorg/vanta">Vanta</a>
          <span class="small-txt" v-if="version">{{version}}</span>, All rights reserved.
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {},
  computed: {
    pagination() {
      return this.$store.state.pagination;
    },
    version() {
      return process.env.BAEL_VERSION || false;
    },
    signupAboutSize: function () {
      return {
        "c-25": this.signupBoolean,
        "c-4": !this.signupBoolean,
      };
    },
    connectData() {
      return this.$store.state.connect;
    },
    siteDescription() {
      return this.$store.state.info.sitedescription;
    },
    signupBoolean() {
      return this.$store.state.info.emailsignup;
    },
  },
};
</script>

<style>
.text-input {
  max-width: 100%;
}
.small-txt {
  font-size: 80%;
}
footer .item:hover .footer__heading {
  color: rgba(119, 119, 119, 0.6);
  transition: 0.2s color ease-in-out;
}
.footer__heading {
  max-width: 100%;
  pointer-events: none;
  color: rgba(119, 119, 119, 0.4);
  font-weight: 800;
  font-size: 85%;
  transition: 0.1s color ease-in-out;
}
.pagination__button--disabled {
  pointer-events: none;
}

.list-unstyled a {
  color: #111111;
  text-transform: uppercase;
  display: block;
  margin-bottom: 8px;
}
</style>
