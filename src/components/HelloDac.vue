<template>
  <div>
    <select v-model="selected">
      <option v-for="(option, index) in options" :key="index" v-bind:value="option.value">
        {{ option.text }}
      </option>
    </select>
    <span>Selected: {{ selected }}</span>
  </div>
</template>

<script>
import EventBus from '@/eventBus'
export default {
  data () {
    return {
      selected: 'A',
      options: [
        { text: 'One', value: 'A' },
        { text: 'Two', value: 'B' },
        { text: 'Three', value: 'C' }
      ],
      nameDac: 'ddd'
    }
  },
  watch: {
    selected() {
      this.sendEventBus()
    }
  },
  methods: {
    sendEventBus() {
      EventBus.$emit('hello', this.selected);
    }
  }
}
</script>
