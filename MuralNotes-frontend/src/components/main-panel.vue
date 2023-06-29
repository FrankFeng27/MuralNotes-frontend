<template>
<StyledContainer>
  <StyledPanelContainer>
    <Sidebar></Sidebar>
    <WorkArea></WorkArea>
  </StyledPanelContainer>
</StyledContainer>
</template>
<script setup lang="ts">
import styled from "vue3-styled-components";

import WorkArea from "./workarea.vue"
import Sidebar from "./sidebar.vue"

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



</script>

