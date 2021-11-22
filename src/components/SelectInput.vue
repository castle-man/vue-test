<template>
  <div>
    <label :for="id">{{ label }}</label>
    <select :id="id" :value="modelValue" v-on:input="$emit('update:modelValue', $event.target.value)">
      <option v-for="option in options" :key="option.value" :value="option.value">
        {{option.text}}
      </option>
    </select>
  </div>
</template>

<script>
  export default {
    name: 'SelectInput',
    props: {
      id: String,
      label: String,
      options: Array,

      // v-model
      modelValue: String
    }
  }
</script>
