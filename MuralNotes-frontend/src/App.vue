<script setup lang="ts">
import { ref } from "vue";
import styled, { ThemeProvider } from "vue3-styled-components";
import { theme } from "./theme/theme";
import MainPanel from "./components/main-panel.vue";

const StyledContainer = styled.div`
  background-color: ${props => props.theme.theme.colors.backColor};
  min-width: 220px;
  min-height: 400px;
  padding: 5px 10px;
  width: 100%;
  height: 100%;
`;

</script>

<template>
  <ThemeProvider :theme={theme}>
    <StyledContainer>
      <MainPanel></MainPanel>
    </StyledContainer>
  </ThemeProvider>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
