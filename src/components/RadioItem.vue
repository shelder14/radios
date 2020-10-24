<template>
  <div>
    <input
      type="radio"
      :value="value"
      :name="name"
      @change="$emit('select-radio', value)"
      :disabled="disabled"
    />
    <label for="">{{ value }}</label>
  </div>
</template>
<script>
export default {
  name: "RadioItem",
  props: {
    value: String,
    name: String,
    disabled: Boolean,
  },
};
</script>