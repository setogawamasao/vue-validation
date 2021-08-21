<template>
  <div>
    <InputComponent />
    <p class="message">メッセージ: {{ msg }}</p>
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
    return { msg: "こんにちは！" };
  },
};
</script>

<style>
.message {
  color: #42b983;
}
</style>
