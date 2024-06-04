<template>
  <div class="gitalk-container">
    <div id="gitalk-container"></div>
  </div>
</template>
<script>
import md5 from "md5";
import Gitalk from "gitalk";
import "gitalk/dist/gitalk.css";
export default {
  name: "gitalk",
  data() {
    return {};
  },
  mounted() {
    const commentConfig = {
      clientID: "Ov23lialPfMZ5Q4aEjKI",
      clientSecret: "2fe3148c4d18fe5df3eaba2ca0b675ea92baec0e",
      repo: "PhilRandWu.github.io",
      owner: "PhilRandWu",
      admin: ["PhilRandWu"],
      id: md5(location.pathname),
      distractionFreeMode: false,
    };
    const gitalk = new Gitalk(commentConfig);
    gitalk.render("gitalk-container");
  },
};
</script>
<style>
.gt-container .gt-header-textarea {
  color: #000;
}
</style>
