<template>
  <div>
    <gradient-settings @gradient-updated="updateGradient"></gradient-settings>
    <gradient-display :startColor="startColor" :endColor="endColor"></gradient-display>
  </div>
</template>

<script>
import GradientSettings from './components/GradientSettings.vue';
import GradientDisplay from './components/GradientDisplay.vue';

export default {
  components: {
    GradientSettings,
    GradientDisplay
  },
  data() {
    return {
      startColor: '#ff0000',
      endColor: '#0000ff'
    };
  },
  methods: {
    updateGradient(data) {
      this.startColor = data.startColor;
      this.endColor = data.endColor;
    }
  }
};
</script>
