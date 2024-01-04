<script>
export default {
  props: {
    favs: {
      type: Array,
      required: true
    },
    getFromFavs: {
      type: Function,
      required: true
    }
  }
}
</script>

<template>
  <h2>Варианты в избранном</h2>
  <div 
    @click="getFromFavs(index)"
    v-for="(el, index) in favs" 
    :key="index"
  >
    <span>{{ el.from }}</span>
    <span>{{ el.to }}</span>
  </div>
</template>

<style scoped>
h2 {
  color: #fff;
}
div {
  display: flex;
  justify-content: space-between;
  width: 500px;
  margin: 10px auto;
  background: #8c00ff;
  transition: .5s ease;
}
span {
  padding: 10px 15px;
  background: #8c00ff;
  color: #fff;
}
div:hover {
  opacity: .7;
  transform: scale(1.1);
  cursor: pointer;
}
</style>