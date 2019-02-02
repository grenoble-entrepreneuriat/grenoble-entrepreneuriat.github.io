<template>
  <div class="section">
    <h3 class="sectionTitleContainer">
      <span class="sectionTitle">{{ title }}</span>
      <ul class="sectionList">
        <app-item
          v-for="item in items"
          v-bind:key="item.url"
          v-bind:url="item.url"
          v-bind:name="item.name"
        />
      </ul>
    </h3>
  </div>
</template>

<script>
import AppItem from "~/components/AppItem.vue";

export default {
  components: {
    AppItem
  },
  props: ["title", "items"]
};
</script>

<style>
.section {
  padding: 20px 10px;
}
.sectionTitle {
  text-transform: uppercase;
  font-size: 1.2em;
  background: #112d4e;
  color: white;
  display: inline-block;
  padding: 5px 12px 2px 12px;
}
.sectionList {
  padding-top: 20px;
  list-style-type: square;
}
</style>
