<template>
  <div>
    <h1>{{ blog_title }}</h1>
    <p v-if="show_post === true">{{ blog_content }}</p>
    <img :src="blog_image_url" alt="blog image" />
    <button @click="injection">CLICK</button>
    <button @click="set_post">show</button>
  </div>
</template>

<script>
export default {
  methods: {
    set_post: function () {
      if (this.show_post === true) {
        this.show_post = false;
      } else {
        this.show_post = true;
      }
    },
    injection: function () {
      document
        .querySelector(`p`)
        .insertAdjacentHTML(`beforeend`, `<p>inserted</p>`);
    },
  },
  data() {
    return {
      blog_content: `blog blog blog blog`,
      blog_title: `BLOG TITLE`,
      blog_image_url: `../src/assets/SwhirlNobackgroundopaque.png`,
      show_post: true,
    };
  },
};
</script>

<style scoped>
</style>
