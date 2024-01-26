<template>
    <div>
      <h2>Настройки градиента</h2>
      <label>Начальный цвет: <input type="color" v-model="startColor" /></label><br />
      <label>Конечный цвет: <input type="color" v-model="endColor" /></label><br />
      <button @click="generateGradient">Сгенерировать градиент</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        startColor: '#ff0000', 
        endColor: '#0000ff'  
      };
    },
    methods: {
      generateGradient() {
        
        this.$emit('gradient-updated', {
          startColor: this.startColor,
          endColor: this.endColor
        });
      }
    }
  };
  </script>
  