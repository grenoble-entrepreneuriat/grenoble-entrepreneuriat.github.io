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

<style>
.itemLabel {
  color: #ec871d;
}
</style>
