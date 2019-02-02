<template>
  <section class="container">
    <header class="header">
      <h1 class="title">Grenoble<br />Entrepreneuriat</h1>
      <h2 class="subtitle">
        Tout sur l'entrepreneuriat grenoblois en un seul endroit.
      </h2>
      <div class="tags">
        <span class="tag">#startup</span>
        <span class="tag">#entrepreneurship</span>
        <span class="tag">#freelance</span> <span class="tag">#pme</span>
      </div>
    </header>
    <div class="main">
      <div v-for="item in sections" v-bind:key="item.name">
        <app-section v-bind:title="item.name" v-bind:items="item.list" />
      </div>
    </div>
    <footer class="footer">
      <a
        href="https://github.com/grenoble-entrepreneuriat/grenoble-entrepreneuriat.github.io/issues"
        class="footer-add"
        target="_blank"
        >Proposer un ajout</a
      >
    </footer>
  </section>
</template>

<script>
import AppLogo from "~/components/AppLogo.vue";
import AppSection from "~/components/AppSection.vue";

import content from "~/assets/content.json";

export default {
  components: {
    AppLogo,
    AppSection
  },
  data() {
    return {
      sections: content.sections
    };
  },
  head: {
    titleTemplate: "Grenoble Entrepreneuriat",
    meta: [
      { charset: "utf-8" },
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      { hid: "description", name: "description", content: "Meta description" }
    ]
  }
};
</script>

<style lang="scss">
.container {
  min-height: 100vh;
  // display: flex;
  // justify-content: center;
  // align-items: center;
  // text-align: center;
}

.header {
  background: white;
  border-bottom: 2px solid #efefef;
  padding: 20px;
}

.footer {
  min-height: 100px;
  background: white;
  border-top: 2px solid #efefef;
  padding: 20px;
  text-align: center;
}

.footer-add {
  color: #959fab;
  text-decoration: none;
  &:hover {
    text-decoration: underline;
  }
}

.main {
  max-width: 950px;
  margin: auto;
}

.title {
  font-family: "Muli", sans-serif;

  // font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
  //   "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 800;
  font-size: 100px;
  color: #2d2b2c;
  letter-spacing: 1px;
  text-align: center;
  font-size: 3em;
  padding: 30px 0px 0px 0px;
  text-transform: uppercase;
  font-weight: bold;

  @media (max-width: 950px) {
    font-size: 30px;
  }
}

.subtitle {
  font-family: "Muli", sans-serif;
  font-weight: 600;
  font-size: 42px;
  color: #ec871d;
  word-spacing: 5px;
  padding: 30px 0;
  text-align: center;
  font-size: 1.8em;
}

.tags {
  color: #959fab;
  font-weight: 600;
  text-transform: uppercase;
  font-size: 1.1em;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;

  .tag {
    background: #eaeef7;
    padding: 5px 10px;
    border-radius: 3px;
    margin: 5px;
  }
}

.links {
  padding-top: 15px;
}
</style>
