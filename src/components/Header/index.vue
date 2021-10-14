<template>
  <div>
    <HeaderTop />
    <HeaderBody />
  </div>
</template>

<script>
import HeaderTop from "./HeaderTop.vue";
import HeaderBody from "./HeaderBody.vue";

export default {
  name: "Header",
  components: {
    HeaderTop,
    HeaderBody,
  },
};
</script>

<style scoped></style>
