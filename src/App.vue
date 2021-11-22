<template>
    <div>
        <SelectInput id="animal-type-select" label="Animal Type" v-model="animalType" :options="typeOptions" />

        <p>
            <Input label="Animal Type" id="animal-type-input" v-model="animalType"/>
        </p>
        <div>
            <h1>Favorite Animal: {{ animalType }}</h1>
        </div>
    </div>
</template>

<script>
import SelectInput from './components/SelectInput.vue'
import Input from './components/Input.vue'

export default {
  name: 'App',
  components: {
    SelectInput,
    Input
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
          input: ''
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
