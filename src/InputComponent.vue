<template>
  <div>
    <input id="input1" v-model="value" type="text" @input="checkEmpty" />
    <div v-if="required">
      必須入力です。
    </div>
  </div>
</template>

<script>
export default {
  name: "InputComponent",
  data() {
    return {
      value: "",
      required: false,
    };
  },
  methods: {
    checkEmpty() {
      this.required = this.value ? false : true;
    },
  },
};
</script>
