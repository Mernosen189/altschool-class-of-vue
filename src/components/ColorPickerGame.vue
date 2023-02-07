<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import { ref, reactive } from "@vue/reactivity";
import myPicker from "../composables/myPicker"

export default {
  setup() {
    const colRef = ref("")

    const { colors, message, matchColor } = myPicker()

    return { colors, message, matchColor }
    
  },
};
</script>

<style></style>
