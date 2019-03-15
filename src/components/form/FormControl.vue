<template>
  <select :id="name" v-if="type === 'select'" class="form-control" @change="onInput">
    <option :value="0">{{placeholder}}</option>
    <option v-for="({ label, value }) in options" :key="value" :value="value">
      {{label}}
    </option>
  </select>

  <textarea :id="name" v-else-if="type === 'textarea'" class="form-control" @input="onInput" />

  <input v-else :type="type" class="form-control" @input="onInput"
    :id="name" :placeholder="placeholder">
</template>

<script>
export default {
  name: 'form-control',
  props: {
    name: {
      type: String,
      required: true
    },
    type: {
      type: String
    },
    placeholder: {
      type: String
    },
    options: {
      type: Array
    }
  },
  mounted () {
    console.log(this.options)
  },
  methods: {
    onInput (ev) {
      this.$emit('input', ev.target.value, ev)
    },
    onChange (ev) {
      this.$emit('change', ev.target.value, ev)
    }
  }
}
</script>
