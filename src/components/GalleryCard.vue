<template>
  <div class="col-md-4">
    <div class="card h-100">
      <img :src="model.imageSrc" class="ratio ratio-4x3" :alt="model.title" />
      <div class="card-body h-100 d-flex flex-column justify-content-between">
        <h5 class="card-title">{{ model.title }}</h5>
        <p class="card-text">{{ model.subtitle }}</p>
        <div class="mt-auto ms-auto">
          <a
            v-for="link in model.links"
            :key="link.id"
            :href="link.href"
            class="text-decoration-none me-2"
            ><Iconfont :name="link.iconfont" :fontSize="'20px'"
          /></a>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from "vue";

import Iconfont from "@/components/Iconfont.vue";

export interface CardLink {
  id: string;
  href: string;
  iconfont: string;
}

export interface CardModel {
  id: string;
  imageSrc: string;
  title: string;
  subtitle: string;
  links: CardLink[];
}

export default defineComponent({
  components: { Iconfont },
  props: {
    model: {
      type: Object as PropType<CardModel>,
      required: true,
    },
  },
});
</script>
