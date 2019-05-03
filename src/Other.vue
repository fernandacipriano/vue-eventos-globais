<template>
  <div>
    Outro component <button @click="dispatchEvent">Disparar evento</button>
    <Child></Child>
  </div>
</template>
<script>
import {eventType} from "./eventType"
import Child from "./Child"

export default {
  name: "Other",
  components: {Child},
  props: ['data'],
  mounted(){
    eventType.$on('app', (result) => {
      console.log(result)
      // this.method()
    })
  },
  methods: {
    dispatchEvent() {
      this.$emit('my-event', 'other component disparou um evento')
    }
  }
}
</script>
<style scoped>
</style>
