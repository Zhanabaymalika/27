<template>
  <div>
    <h2>Результат градиента</h2>
    <div :style="{background: 'linear-gradient(to right, ' + startColor + ', ' + endColor + ')', height: '100px'}"></div>
  </div>
</template>

<script>
export default {
  props: {
    startColor: String,
    endColor: String
  }
};
</script>
