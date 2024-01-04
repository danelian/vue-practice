<script>
export default {
  props: {
    changeAmount: {
      type: Function,
      required: true
    },
    convert: {
      type: Function,
      required: true
    }
  }
}
</script>

<template>
  <input min="0" type="number" @input="changeAmount($event.target.value)">
  <button @click="convert()">Конвертировать</button>
</template>

<style scoped>
input {
  outline: none;
  width: 560px;
  position: relative;
  top: -50px;
  font-size: 1.25em;
  border-radius: 5px;
  border: 4px solid #1a032d;
  padding: 15px 20px;
  color: #333;
  background: #fafafa;
}
button {
  position: relative;
  top: -20px;
  display: flex;
  margin: auto;
  padding: 15px 20px;
  color: #fff;
  text-transform: uppercase;
  cursor: pointer;
  background: #1a032d;
  border: 0;
  border-radius: 3px;
}
</style>