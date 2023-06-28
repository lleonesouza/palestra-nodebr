<template>
    <div class="gif-container" :class="{ 'gif-container-hidden': hidden }">
      <img  v-if="!hidden" :src="gifSrc" :alt="altText" />
    </div>
  </template>
  
  <script>
  export default {
    props: {
      gifSrc: {
        type: String,
        required: true
      },
      altText: {
        type: String,
        required: true
      },
      hidden: {
        type: Boolean,
        default: false
      },
      next: {
        type: Boolean,
        default: false
      }
    },
    mounted() {
      if (!this.hidden) {
        setTimeout(() => {
          this.$emit('show-next-gif');
        }, 4000);
      }
    }
  };
  </script>
  
  <style>
  .gif-container {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100%;
    transition: opacity 1s ease;
  }
  
  .gif-container-hidden {
    opacity: 0;
  }
  </style>
  