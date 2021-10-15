<template>
  <div id="home">
    <Header />
    <Carousel />
    <Provide />
    <Selective />
    <Story />
    <Helper />
  </div>
</template>

<script>
import Header from "../../components/Header";
import Carousel from "./Carousel";
import Provide from "./Provide";
import Selective from "./Selective";
import Story from "./Story";
import Helper from "./Helper";

export default {
  name: "Home",
  components: {
    Header,
    Carousel,
    Provide,
    Selective,
    Story,
    Helper,
  },
};
</script>

<style></style>
