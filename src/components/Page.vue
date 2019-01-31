<template >
  <div class="page">
    <span class="contact">Contact</span>
    <target-link class="link twitter" v-bind:text="texts.twitter" v-bind:href="hrefs.twitter"></target-link>
    <target-link class="link dribbble" v-bind:text="texts.dribbble" v-bind:href="hrefs.dribbble"></target-link>
    <target-link class="link codepen" v-bind:text="texts.codepen" v-bind:href="hrefs.codepen"></target-link>
    <target-link class="link weibo" v-bind:text="texts.weibo" v-bind:href="hrefs.weibo"></target-link>
  </div>
</template>

<script>
import TargetLink from "./TargetLink.vue";

const texts = {
  twitter: "twitter",
  dribbble: "dribbble",
  codepen: "codepen",
  weibo: "weibo"
};

const hrefs = {
  twitter: "https://twitter.com/JHWviuDZH8bcvuM",
  dribbble: "https://dribbble.com/De_Coder",
  codepen: "https://codepen.io/De-Coder/",
  weibo: "https://weibo.com/3229623314"
};

export default {
  name: "Page",
  data() {
    return {
      texts: texts,
      hrefs: hrefs
    };
  },
  components: {
    TargetLink
  }
};
</script>

<style lang="scss" scoped>
$white: #ffffff;
$blue: #1ba1f3;
$pink: #ea4c89;
$qing: #5effdb;
$red: #f42a2f;
.page {
  flex-shrink: 0;
  width: 100vw;
  height: 100vh;
  background-color: black;
  display: grid;
  grid-template-rows: 10rem 1fr;
  grid-template-columns: repeat(4, 1fr);
  justify-items: center;
  align-items: center;
}
.link {
  font-family: "neon";
  font-weight: 800;
}
.twitter {
  color: $blue;
  text-shadow: 0 0 3vw $blue;
}
.dribbble {
  color: $pink;
  text-shadow: 0 0 3vw $pink;
}
.codepen {
  color: $qing;
  text-shadow: 0 0 3vw $qing;
}
.weibo {
  color: $red;
  text-shadow: 0 0 3vw $red;
}
.contact {
  border: 0.2rem solid $white;
  border-radius: 0rem 0rem 1rem 1rem;
  padding: 1rem 2rem;
  box-shadow: 0 0 3vw $white;

  color: $white;
  font-size: 2rem;
  text-shadow: 0 0 1vw $white;

  grid-row: 1/2;
  grid-column: 1/5;
  align-self: start;
  transform: translateY(-0.4rem);
}
</style>