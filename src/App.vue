<template>
  <div id="app">
    <form action="">
      <RadioGroup v-for="(item, key) in radioGroups" :key="key" v-bind="item" />
    </form>
  </div>
</template>
<script>
import RadioGroup from "./components/RadioGroup.vue";
export default {
  name: "App",
  components: {
    RadioGroup,
  },
  data() {
    return {
      radioGroups: [
        {
          name: "radio1",
          disabled: true,
          radios: ["radio1Value1", "radio1Value2"],
        },
        {
          name: "radio2",
          disabled: false,
          radios: ["radio2Value1", "radio2Value2"],
        },
        {
          name: "radio3",
          disabled: false,
          radios: [
            "radio3Value1",
            "radio3Value2",
            "radio3Value3",
            "radio3Value4",
          ],
        },
      ],
    };
  },
};
</script>