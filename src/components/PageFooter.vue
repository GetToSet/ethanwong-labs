<template>
  <div class="container footer">
    <footer class="py-3 my-4">
      <p class="text-center text-muted">
        Copyright &copy; 2020-2022 Ethan Wong, All rights reserved.
      </p>
    </footer>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  components: {},
  setup() {
    return;
  },
});
</script>

<style scoped lang="scss">
.footer {
  position: sticky;
  top: 100vh;
}
</style>
