<template>
  <div v-html="markedContent"></div>
</template>

<script>
import marked from "marked";
import markDownSource from "./md/03.md";

export default {
  computed: {
    source() {
      return markDownSource;
    },
    markedContent() {
      return marked(this.source);
    },
  },
};
</script>

<style>
</style>