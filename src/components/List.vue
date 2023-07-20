<template>
  <template v-for="name in names" :key="name.firstName">
    <slot :firstName="name.firstName" :lastName="name.lastName"></slot>
  </template>
</template>
<script>
export default {
  name: "List",
  data() {
    return {
      names: [
        {
          firstName: "D",
          lastName: "M",
        },
        {
          firstName: "Der",
          lastName: "Mwe",
        },
        {
          firstName: "Dero",
          lastName: "Mwema",
        },
      ],
    };
  },
};
</script>
<style>
</style>