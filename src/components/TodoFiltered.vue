<template>
  <div>
    <button :class="{ active: filter == 'all' }" @click="changeFilter('all')">
      全てのタスク
    </button>
    <button
      :class="{ active: filter == 'active' }"
      @click="changeFilter('active')"
    >
      取組中のタスク
    </button>
    <button
      :class="{ active: filter == 'completed' }"
      @click="changeFilter('completed')"
    >
      完了したタスク
    </button>
  </div>
</template>

<script>
export default {
  name: "todo-filtered",
  computed: {
    filter() {
      return this.$store.state.filter;
    },
  },
  methods: {
    changeFilter(filter) {
      this.$store.dispatch("updateFilter", filter);
    },
  },
};
</script>
