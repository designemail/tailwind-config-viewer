<template>
  <div class="flex flex-wrap -mb-4">
    <div
      v-for="(value, prop) in data"
      :key="prop"
      class="mr-4 mb-4"
    >
      <div
        class="mb-2 w-40 h-40 bg-gray-200 border-gray-400"
        :style="{
          borderWidth: value
        }"
      />
      <CanvasBlockLabel
        :label="`${removeDefaultSuffix(`border-${prop}`)}`"
        :value="value"
      />
    </div>
  </div>
</template>

<script>
import CanvasBlockLabel from '../CanvasBlockLabel'
import { removeDefaultSuffix } from '@/utils'

export default {
  components: {
    CanvasBlockLabel
  },

  props: {
    data: {
      type: Object,
      required: true
    }
  },

  methods: {
    removeDefaultSuffix
  }
}
</script>
