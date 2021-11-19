<template>
  <SelectInput id="animal-type" label="Animal Type" :currentValue="animalType" :options="typeOptions"/>
</template>

<script>
import SelectInput from './components/SelectInput.vue'

export default {
  name: 'App',
  components: {
    SelectInput
  },
  data: function() {
      return {
          typeOptions: [
                { text: 'Dog', value: 'dog' },
                { text: 'Cat', value: 'cat' },
                { text: 'Cow', value: 'cow' },
                { text: 'Pig', value: 'pig' }
          ],
          animalType: 'dog',
      }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
