<template>
  <div class="alert alert-primary">
    <h1>{{ title }}</h1>
    <p>{{ msg }}</p>
  </div>
</template>

<script>
import { h, ref } from "vue";

export default {
  props: {
    title: String,
    msg: String,
  },
  setup(props) {
    return () =>
      h("div", { class: "alert alert-primary" }, [
        h("h1", props.title),
        h("p", props.msg),
      ]);
  },
};
</script>