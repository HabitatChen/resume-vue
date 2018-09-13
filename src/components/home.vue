<template>
  <div>
    <home-header></home-header>
    <home-banner></home-banner>
    <home-card></home-card>
    <home-skill></home-skill>
    <home-project></home-project>
  </div>

</template>

<script>
import HomeHeader from "@/components/childComponents/header";
import HomeBanner from "@/components/childComponents/banner";
import HomeCard from "@/components/childComponents/card";
import HomeSkill from "@/components/childComponents/skill";
import HomeProject from "@/components/childComponents/project";
export default {
  name: "Home",
  components: {
    HomeHeader,
    HomeBanner,
    HomeCard,
    HomeSkill,
    HomeProject
  },
  data () {
    return {
      swiperList:[]
    }
  }
};
</script>

<style lang="stylus" >
.clearfix::after {
  content: '';
  display: block;
  clear: both;
}

* {
  padding: 0;
  margin: 0;
}

hr {
  height: 0;
  border: none;
  border-top: 1px solid #dedede;
}

ul, ol {
  list-style: none;
}

h1, h2, h3, h4, h5, h6 {
  font-weight: normal;
}

body {
  background: #efefef;
  color: black;
  margin: 0;
}

a {
  color: inherit;
  text-decoration: none;
}
</style>
