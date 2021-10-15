<template>
  <div id="home">
    <Header />
    <Carousel />
    <Provide />
    <Selective />
    <Story />
    <Helper />
    <Contact />
    <News />
    <Enterprise />
    <Footer />
  </div>
</template>

<script>
import Header from "../../components/Header";
import Carousel from "./Carousel";
import Provide from "./Provide";
import Selective from "./Selective";
import Story from "./Story";
import Helper from "./Helper";
import Contact from "./Contact";
import News from "./News";
import Enterprise from "./Enterprise";
import Footer from "../../components/Footer";

export default {
  name: "Home",
  components: {
    Header,
    Carousel,
    Provide,
    Selective,
    Story,
    Helper,
    Contact,
    News,
    Enterprise,
    Footer,
  },
};
</script>

<style></style>
