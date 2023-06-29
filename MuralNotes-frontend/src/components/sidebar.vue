<template>
<StyledSidebarContainer>
  <StyledInputContainer>
    <n-input type="text" placeholder="search"></n-input>
  </StyledInputContainer>
  <StyledTagsContainer>
  <n-collapse default-expanded-names="alltags">
    <n-collapse-item title="All tags" name="alltags">
      <StyledTagItem><div># memos</div></StyledTagItem>
      <StyledTagItem><div># aws</div></StyledTagItem>
    </n-collapse-item>
  </n-collapse>
  </StyledTagsContainer>
</StyledSidebarContainer>
</template>
<script setup lang="ts">
import styled from "vue3-styled-components";
import { NCollapse, NCollapseItem, NInput } from "naive-ui";

const StyledSidebarContainer = styled.div`
  flex-grow: 0;
  width: 300px;
  display: flex;
  flex-direction: column;
  padding: 5px 15px;
`;
const StyledInputContainer = styled.div`
  margin: 5px 10px;
`;
const StyledTagsContainer = styled.div`
  margin: 5px 10px;
`;
const StyledTagItem = styled.div`
  padding: 2px 10px 2px 20px;
`;
</script>