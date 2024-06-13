<template>
  <div>
    <h1 :class="{ 'highlight': isHighlighted }">Masukkan Teks</h1>
    <p :style="{ fontSize: fontSize + 'px', color: textColor }">teks akan muncul</p>
    <input type="text" v-model="textInput" @input="updateText">
    <p :style="{ fontSize: fontSize + 'px', color: textColor }">{{ textInput }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isHighlighted: false,
      fontSize: 16,
      textColor: '#000000',
      textInput: ''
    }
  },
  methods: {
    updateText(event) {
      this.textInput = event.target.value;
    }
  }
}
</script>

<style scoped>
.highlight {
  background-color: rgb(0, 17, 255);
}
</style>
