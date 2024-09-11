<script setup lang="ts">
//import TheWelcome from '../components/TheWelcome.vue'
import { ref } from 'vue'
import window from '../components/dialogWindow.vue'

const isPopupVisible = ref(false);

const showPopup = () => {
  isPopupVisible.value = true;
};

const closePopup = () => {
  isPopupVisible.value = false;
}

</script>

<template>
  <div class="main">
    <button class="alert" @click="showPopup">
      Dialog Alert
    </button>
    <window v-if="isPopupVisible" @close="closePopup"></window>
  </div>
</template>
<style scoped>
.main button {
  padding: 0.8rem;
  background-color: red;
  color: white;
  font-size: 1rem;
  font-weight: 600;
  border-color: white;
  border-radius: 10px;
}
</style>
