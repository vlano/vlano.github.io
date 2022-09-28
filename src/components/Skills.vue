<template>
  <section>
    <Skill title="Unity" imageUrl="/unityLogo.svg" experience="5+ years"/>
    <Skill title="C#" imageUrl="/cSharpLogo.svg" experience="5+ years"/>
    <Skill title="Git" imageUrl="/gitLogo.svg" experience="5+ years"/>
    <Skill title="JavaScript" imageUrl="/jsLogo.svg" experience="3+ years"/>
    <Skill title="Vue.js" imageUrl="/vueLogo.svg" experience="2+ years"/>
  </section>
</template>

<script>
import Skill from "./Skill.vue";

export default {
  name: "Skills",
  components: {Skill}
}
</script>

<style scoped>
section {
  height: 14rem;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  background: linear-gradient(90deg, var(--dark-purple) 0%, var(--dark-blue) 100%);
}


</style>