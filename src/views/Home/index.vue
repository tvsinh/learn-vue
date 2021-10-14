<template>
  <div id="home">
    <Header />
    <Carousel />
    <Provide />
  </div>
</template>

<script>
import Header from "../../components/Header";
import Carousel from "./Carousel";
import Provide from "./Provide";

export default {
  name: "Home",
  components: {
    Header,
    Carousel,
    Provide,
  },
};
</script>

<style></style>
