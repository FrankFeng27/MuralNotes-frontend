<template>
<StyledSidebarContainer>
  <n-collapse default-expanded-names="alltags">
    <n-collapse-item title="All tags" name="alltags">
      <div># memos</div>
      <div># aws</div>
    </n-collapse-item>
  </n-collapse>
</StyledSidebarContainer>
</template>
<script setup lang="ts">
import styled from "vue3-styled-components";
import { NCollapse, NCollapseItem } from "naive-ui";

const StyledSidebarContainer = styled.div`
  flex-grow: 0;
  width: 300px;
`;
</script>