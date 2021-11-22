<template>
  <div>
    <label :for="id">{{ label }}</label>
    <input :id="id" :value="modelValue" @input="$emit('update:modelValue', $event.target.value)"/>
  </div>
</template>

<script>
  export default {
    name: 'Input',
    props: {
        modelValue: String,
        label: String
    },
    emits: ['update:modelValue'],

  }
</script>
