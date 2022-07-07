<template>
  <div>Home{{ Next }}</div>
  <button @click="Plus">Onee</button>
</template>
<script>
export default {
  data() {
    return {
      Data: 4,
    };
  },
  computed: {
    Next() {
      return this.Data;
    },
  },
  methods: {
    Plus() {
      this.Data++;
    },
  },
  setup() {
    useHead({
      titleTemplate: "%s - useHead example",
      bodyAttrs: {
        class: "test",
      },
    });
    return { dynamic: ref(49) };
  },
  head: {
    title: "Another title",
  },
};
</script>