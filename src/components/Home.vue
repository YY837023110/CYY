<template>
  <div>
    <app-banner :listImgs="listImg"></app-banner>
  </div>
</template>

<script>
import Banner from "./Banner.vue";
import a from "../../static/img/home/1.jpg";
import b from "../../static/img/home/2.jpg";
import c from "../../static/img/home/3.jpg";
import d from "../../static/img/home/4.jpg";
import e from "../../static/img/home/5.jpg";
export default {
  name: "Home",
  mounted () {
    console.log(this.listImg)
  },
  data() {
    return {
      listImg: [
        {
          url: a
        },
        {
          url: b
        },
        {
          url: c
        },
        {
          url: d
        },
        {
          url: e
        }
      ]
    };
  },
  components: {
    "app-banner": Banner
  }
};
</script>

<style>

</style>
