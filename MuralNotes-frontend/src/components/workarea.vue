<template>
<StyledWorkContainer>
  <a href="https://vitejs.dev" target="_blank">
    <img src="/vite.svg" class="logo" alt="Vite logo" />
  </a>
  <a href="https://vuejs.org/" target="_blank">
    <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
  </a>
  <HelloWorld msg="Vite + Vue" />
</StyledWorkContainer>
</template>
<script setup lang="ts">
import styled from "vue3-styled-components";

import HelloWorld from "./HelloWorld.vue";

const StyledWorkContainer = styled.div`
  flex-grow: 10;
  min-width: 300px;
  max-width: 800px;
`;

</script>