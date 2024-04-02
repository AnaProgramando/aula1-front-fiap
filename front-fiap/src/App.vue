<script setup>
import HelloWorld from './components/HelloWorld.vue'
import { ref, computed} from 'vue';
import LoginPage from './components/LoginPage.vue';
import PageNotFound from './components/PageNotFound.vue';

const routes = {
  '/': LoginPage,
  '': LoginPage,
}

const currentPath = ref(window.location.hash);

window.addEventListener('hashchange', () => {
  currentPath.value = window.location.hash;
})

const currentView = computed(() => 
  routes[currentPath.value.slice(1)] || PageNotFound)

</script>

<template>
  <component :is="currentView"/>
</template>
