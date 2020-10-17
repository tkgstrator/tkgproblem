<template>
  <div v-html="markedContent"></div>
</template>

<script>
import marked from "marked";
import markDownSource from "./md/index.md";

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
@import url("https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@500&display=swap");

#app {
  font-family: "Noto Sans JP", sans-serif;
}

.container {
  text-align: center;
  width: 90%;
}

ul {
  font-size: 1.5vw;
  list-style: none;
}

h2 {
  padding-bottom: 20px;
}
</style>