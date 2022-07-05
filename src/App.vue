<template>
  <PageRoot class="page-root" />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import PageRoot from "@/pages/PageRoot.vue";

export default defineComponent({
  components: {
    PageRoot,
  },
});
</script>

<style lang="scss">
@import "@/scss/bootstrap.scss";
@import "@/scss/fonts.scss";
html,
body,
#app {
  height: 100%;
}
</style>
