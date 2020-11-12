<template>
  <div>残りのタスク{{ remaining }}個</div>
</template>

<script>
export default {
  name: "todo-remaining",
  computed: {
    remaining() {
      return this.$store.getters.remaining;
    },
  },
};
</script>
