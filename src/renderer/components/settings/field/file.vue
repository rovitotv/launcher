<template>
    <div class="six wide field">
        <label>{{ field.display || field.name }}:</label>
        <input
            type="file"
            :name="field.name"
            :value="value"
            :accept="field.extensions"
            @change="$emit('value-change', $event.target.value)"
        />
    </div>
</template>

<script>
  export default {
    name: 'file-field',
    props: ['field', 'value']
  }
</script>

<style scoped>

</style>
