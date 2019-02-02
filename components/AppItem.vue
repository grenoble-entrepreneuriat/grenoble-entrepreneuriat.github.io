<template>
  <li class="item">
    <a class="itemLabel" target="_blank" v-bind:href="url">{{ name }}</a>
  </li>
</template>

<script>
export default {
  props: ["name", "url", "description"]
};
</script>

<style lang="scss">
.itemLabel {
  color: #ec871d;
  text-decoration: none;
  &:hover {
    text-decoration: underline;
  }
}
</style>
