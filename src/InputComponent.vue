<template>
  <div>
    <input
      :type="type"
      :name="name"
      :value="value"
      :placeholder="placeholder"
      @input="checkEmpty"
    />
    <div v-if="required">
      必須入力です。
    </div>
  </div>
</template>

<script>
export default {
  name: "InputComponent",
  props: {
    value: { type: String, required: true },
    type: { type: String, required: true },
    name: { type: String, required: true },
    placeholder: { type: String, required: false },
  },
  data() {
    return {
      required: false,
    };
  },
  methods: {
    checkEmpty(event) {
      this.$emit("input", event.target.value);
      this.required = event.target.value ? false : true;
    },
  },
};
</script>
