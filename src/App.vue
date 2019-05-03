<template>
  <div>
    App <button @click="dispatchEvent">Disparar evento</button>
    <Other v-on:my-event="onMyEventDispatched" :data="variavel"></Other>
  </div>
</template>

<script>
import Other from "./Other"
import {eventType, TYPE1} from "./eventType"
export default {
  name: 'app',
  components: {
    Other
  },
  data () {
    return {
      variavel: ''
    }
  },
  methods: {
    onMyEventDispatched($event) {
      console.log($event)
    },
    dispatchEvent (){
      eventType.$emit('app', 'app disparou um evento')
      eventType.$emit(TYPE1 , 'app disparou um evento')
    }
  }
}
</script>

<style>

</style>
