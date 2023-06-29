<template>
<StyledWorkContainer>
  <Editor
   api-key="ofajqdu0x6g64n4wbwj2nbcfeu44iymvrd3kg59bj7mfocts"
   :init="{
        plugins: 'lists link image table code help wordcount',
        toolbar: 'undo redo | formatselect | bold italic | alignleft aligncenter alignright alignjustify | bullist numlist | table | image | link',
        menubar: false,
        setup: (editor: any) => {
          editor.on('Change', (e:any) => (onContentChange(e, editor)));
        }
      }"
    />
</StyledWorkContainer>
</template>
<script setup lang="ts">
import styled from "vue3-styled-components";
import Editor from "@tinymce/tinymce-vue";


const StyledWorkContainer = styled.div`
  flex-grow: 10;
  min-width: 300px;
  max-width: 800px;
`;

function onContentChange(_event: any, editor: any) {
  console.log("content changed");
  const cnt = editor.getContent();
  console.log(`content: ${cnt}`);
}

</script>