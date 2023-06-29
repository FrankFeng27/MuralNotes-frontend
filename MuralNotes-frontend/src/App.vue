<script setup lang="ts">
import { ref } from "vue";
import styled, { ThemeProvider } from "vue3-styled-components";
import { NCollapse, NCollapseItem } from "naive-ui";

import { theme } from "./theme/theme";
import HelloWorld from './components/HelloWorld.vue'

const StyledContainer = styled.div`
  background-color: ${props => props.theme.theme.colors.backColor};
  min-width: 220px;
  min-height: 400px;
  padding: 5px 10px;
  width: 100%;
  height: 100%;
`;

const StyledPanelContainer = styled.div`
  margin: 0 auto;
  max-width: 1280px;
  height: 100%;
  display: flex;
  flex-direction: row;
`;

const StyledSidebarContainer = styled.div`
  flex-grow: 0;
  width: 300px;
`;

const StyledWorkContainer = styled.div`
  flex-grow: 10;
  min-width: 300px;
  max-width: 800px;
`;



</script>

<template>
  <ThemeProvider :theme={theme}>
    <StyledContainer>
      <StyledPanelContainer>
        <StyledSidebarContainer>
          <n-collapse default-expanded-names="1">
            <n-collapse-item title="All tags">
              <div># memo</div>
              <div># aws</div>
            </n-collapse-item>
          </n-collapse>
        </StyledSidebarContainer>
        <StyledWorkContainer>
        <a href="https://vitejs.dev" target="_blank">
          <img src="/vite.svg" class="logo" alt="Vite logo" />
        </a>
        <a href="https://vuejs.org/" target="_blank">
          <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
        </a>
        <HelloWorld msg="Vite + Vue" />
      </StyledWorkContainer>
      </StyledPanelContainer>
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
