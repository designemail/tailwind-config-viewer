<template>
  <div class="space-y-4">
    <div
      v-for="(value, prop) in data"
      :key="prop"
    >
      <div class="mb-2 bg-gray-200">
        <div
          class="bg-gray-400"
          :style="{
            maxWidth: value,
            height: '100px'
          }"
        />
      </div>
      <CanvasBlockLabel
        :label="`min-w-${prop}`"
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
