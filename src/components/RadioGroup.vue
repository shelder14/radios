<template>
  <div>
      {{name}}
      <RadioItem v-for="(item, index) in radios" :key="index" @select-radio="selectRadio($event)" :disabled="disabled"  :value="item" :name="name"  />
      Selected: {{selected}}
      <br>
      <br>
  </div>
</template>

<script>
import RadioItem from '@/components/RadioItem.vue'
export default {
  name: 'RadioGroup',
  props: {
    disabled: Number,
    name: String,
    radios: Array
  },
  components: {
    RadioItem
  },
  data() {
    return {
      selected: ""
    }
  },
  methods: {
    selectRadio(value) {
      this.selected = value;
       
    }
  }
}
</script>
