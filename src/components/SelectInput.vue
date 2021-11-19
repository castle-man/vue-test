<template>
  <div>
    <label :for="id">{{label}}</label>
    <select :id="id" :value="currentValue" @input="$emit('input', $event.target.value)">
      <option v-for="option in options" :key="option.value" :value="option.value">
        {{option.text}}
      </option>
    </select>
    <p>length: {{ currentValue }}</p>
  </div>
</template>

<script>
  export default {
    name: 'SelectInput',
    props: {
      id: String,
      label: String,
      options: Array,
      currentValue: String
    }
  }
</script>
