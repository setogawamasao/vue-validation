<template>
  <div>
    <InputComponent
      v-model="sampleForm.text1"
      placeholder="サンプル1"
      name="sample-input1"
      type="text1"
    />
    <p class="message">メッセージ: {{ sampleForm.text1 }}</p>
    <InputComponent
      v-model="sampleForm.text2"
      placeholder="サンプル2"
      name="sample-input2"
      type="text2"
    />
    <p class="message">メッセージ: {{ sampleForm.text2 }}</p>
  </div>
</template>

<script>
import InputComponent from "./InputComponent.vue";
export default {
  name: "app",
  components: {
    InputComponent,
  },
  data() {
    return { sampleForm: { text1: "", text2: "" } };
  },
};
</script>

<style>
.message {
  color: #42b983;
}
</style>
