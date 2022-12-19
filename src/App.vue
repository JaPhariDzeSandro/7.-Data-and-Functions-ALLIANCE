<template>
  <h2>My Course Goal</h2>
  <h3 v-if="visibility">{{ mainGoal }}</h3>
  <button @click="toggleButton">Toggle Goal</button>
</template>

<script>
import { ref } from 'vue';
export default {
  setup() {
    const mGoal = ref('Master vuejs!');
    const visibility = ref(true);

    function tbutton() {
      visibility.value = !visibility.value;
    }

    return { mainGoal: mGoal, toggleButton: tbutton, visibility: visibility };
  },
};
</script>
<!--
<template>
  <h2>My Course Goal</h2>
  <h3 v-if="visibility">{{ mainGoal }}</h3>
  <button @click="toggleButton">Toggle Goal</button>
</template>

<script>
export default {
  data() {
    return {
      visibility: true,
      mainGoal: 'Master vuejs!',
    };
  },
  methods: {
    toggleButton() {
      this.visibility = !this.visibility;
    }
  }
};
</script>
-->
<!--
<template>
  <h2>My Course Goal</h2>
  <h3 v-if="mGoal.visibility">{{ mGoal.mainGoal }}</h3>
  <button @click="toggleButton">Toggle Goal</button>
</template>

<script setup>
import { reactive } from 'vue';

const mGoal = reactive({
  mainGoal: 'Master vuejs!',
  visibility: true
});

function toggleButton() {
  mGoal.visibility = !mGoal.visibility
}

</script>
-->
<style>
html {
  font-family: sans-serif;
}
body {
  margin: 3rem;
  text-align: center;
}
</style>
