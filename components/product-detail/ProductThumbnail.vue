<template>
  <div class="w-full min-h-full h-full flex items-center justify-center">
    <img
      v-if="hasImage"
      :src="src"
      class="object-contain p-4"
    >
    <p
      v-if="!hasImage"
      class="text-center"
    >There is no image available.</p>
  </div>
</template>

<script>
export default {
    name: 'ProductThumbnail',
    props: {
        src: {
            type: String, 
            required: true,
        }
    },
    computed: {
        hasImage() {
            return this.src;
        }
  }
}
</script>
