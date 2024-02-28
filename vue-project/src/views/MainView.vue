<template>
  <div class="container">
    <button
      class="container_item"
      v-for="item in numbers"
      :key="item.id"
      @click="clickButton(item)"
    >
      {{ item }}
    </button>
  </div>
  <p>{{ message }}</p>
</template>

<script>
export default {
  data() {
    return {
      numbers: [1, 2, 3, 4, 5, 6, 7, 8, 9],
      message: ''
    }
  },
  methods: {
    clickButton(item) {
      this.message = 'El butón presionat es el ' + item
      console.log(buttonPressed)
    }
  }
}
</script>

<style scoped>
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  padding: 20px;
}

.container_item {
  background-color: #555;
  color: #fff;
  padding: 10px;
  margin: 5px;
  border: none;
  border-radius: 5px;
}

.container_item:hover {
  background-color: #777;
}

.container_item:focus {
  outline: none;
  box-shadow: 0 0 5px #fff;
}
</style>
