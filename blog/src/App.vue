<script lang="ts">
import SimpleGallery from "./components/SimpleGallery.vue";

export default {
  components: {
    SimpleGallery,
  },
  data() {
    return {
      images: this.imagesListF(),
      windowWidth: window.innerHeight,
      windowHeight: window.innerHeight,
    };
  },
  _methods: {
    imagesListF() {
      const imagesList = [];
      for (let i = 1; i < 3; i++) {
        const image = { url: "picture/" + i + ".jpg"};
        imagesList.push(image);
      }
      return imagesList;
    },
  },
  get methods() {
    return this._methods;
  },
  set methods(value) {
    this._methods = value;
  },
};
</script>

<template>
  <div class="center">
    <h1>Stavba plachetnice</h1>
    <p></p>

    <SimpleGallery
      class="gallery"
      galleryID="my-test-gallery"
      :images="images"
      :height="windowHeight"
      :width="windowWidth"
    />
  </div>
</template>

<style scoped>
.center {
  text-align: center;
}
.center h1 {
  margin-top: 40px;
  margin-bottom: 40px;
}
.gallery {
  display: flex;
  flex-direction: column;
}
</style>
