<template>
  <div>
    Filho
  </div>
</template>
<script>
import {eventType, TYPE1} from "./eventType"

export default {
  name: "Child",
  mounted(){
    // eventType.$on('app', (result) => {
    //   console.log(result)
    // })
    eventType.$on(TYPE1, (result) => {
      console.log(result)
    })
  },
}
</script>
<style scoped>
</style>
