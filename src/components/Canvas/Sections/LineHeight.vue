<template>
  <div class="divide-y -my-4">
    <div
      v-for="(value, prop) in data"
      class="py-4"
      :key="prop"
    >
      <div
        class="text-lg mb-2"
        :style="{
          lineHeight: value
        }"
      >
        <p>The quick brown fox jumped over the lazy dog.</p>
        <p>The quick brown fox jumped over the lazy dog.</p>
      </div>
      <CanvasBlockLabel
        :label="`leading-${prop}`"
        :value="value"
      />
    </div>
  </div>
</template>

<script>
import CanvasBlockLabel from '../CanvasBlockLabel'

export default {
  components: {
    CanvasBlockLabel
  },
  props: {
    data: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.row:not(:last-child) {
  @apply border-b;
}
</style>
