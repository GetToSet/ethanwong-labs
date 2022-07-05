<template>
  <div class="page-root">
    <PageHeader />
    <div class="container">
      <div class="my-5 d-flex justify-content-start align-items-center">
        <img
          class="d-block"
          src="@/assets/tube.png"
          alt=""
          width="120"
          height="120"
        />
        <div class="ms-4">
          <h1 class="display-5 fw-bold mb-1">Laboratory</h1>
          <p class="lead fst-italic mb-0">
            <strong>noun.</strong> a place to experiment and try new ideas.
          </p>
        </div>
      </div>
      <div class="row g-3">
        <GalleryCard v-for="card in cards" :key="card.id" :model="card" />
      </div>
    </div>
    <PageFooter />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

import PageHeader from "@/components/PageHeader.vue";
import GalleryCard, { CardModel } from "@/components/GalleryCard.vue";
import PageFooter from "@/components/PageFooter.vue";

import thumbnailGallery from "@/assets/thumbnails/photo-gallery.jpg";
import thumbnailEthanwongV2 from "@/assets/thumbnails/ethanwong-v2.jpg";
import thumbnailEthanwongV1 from "@/assets/thumbnails/ethanwong-v1.jpg";
import thumbnailUnderConstruction from "@/assets/thumbnails/under-construction.jpg";

const cards: CardModel[] = [
  {
    id: "photo-gallery",
    imageSrc: thumbnailGallery,
    title: "Photo Gallery",
    subtitle: "My personal photo gallery",
    links: [
      {
        id: "github",
        href: "https://github.com/GetToSet/ethanwong-photo-gallery/",
        iconfont: "github",
      },
      {
        id: "link",
        href: "https://gallery.ethanwong.me/",
        iconfont: "earth",
      },
    ],
  },
  {
    id: "homepage-v2",
    imageSrc: thumbnailEthanwongV2,
    title: "Home Page V2",
    subtitle: "My personal homepage (2021 - Today).",
    links: [
      {
        id: "github",
        href: "https://github.com/GetToSet/ethanwong.me/",
        iconfont: "github",
      },
      {
        id: "link",
        href: "https://ethanwong.me/",
        iconfont: "earth",
      },
    ],
  },
  {
    id: "homepage-v1",
    imageSrc: thumbnailEthanwongV1,
    title: "Home Page V1",
    subtitle: "My personal homepage (2018 - 2021).",
    links: [
      {
        id: "link",
        href: "https://static.ethanwong.me/labs/ethanwong-v1/",
        iconfont: "earth",
      },
    ],
  },
  {
    id: "under-construction",
    imageSrc: thumbnailUnderConstruction,
    title: "Under Construction",
    subtitle: 'A clean and beautiful static site for "Under Construction".',
    links: [
      {
        id: "github",
        href: "https://github.com/GetToSet/under-construction/",
        iconfont: "github",
      },
      {
        id: "link",
        href: "https://static.ethanwong.me/labs/under-construction/",
        iconfont: "earth",
      },
    ],
  },
];

export default defineComponent({
  components: { GalleryCard, PageHeader, PageFooter },
  setup() {
    return {
      cards,
    };
  },
});
</script>

<style scoped lang="scss">
.page-root {
  height: 100%;
}
</style>
