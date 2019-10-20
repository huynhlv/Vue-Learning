<template>
  <div>
    {{ nameNeo }}
  </div>
</template>

<script>
import EventBus from '@/eventBus'
export default {
  data () {
    return {
      nameNeo: 'nnnn'
    }
  },
  created() {
    // Listening the event hello
    EventBus.$on('hello', this.handler);
  },
  destroyed() {
    // Stop listening the event hello with handler
    EventBus.$off('hello', this.handler);
  },
  methods: {
    handler(e) {
      this.nameNeo = e
      alert(e)
    }
  }
}
</script>
