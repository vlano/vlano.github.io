<template>
  <section>
    <Skill title="Unity" imageUrl="/unityLogo.svg" experience=""/>
    <Skill title="C#" imageUrl="/cSharpLogo.svg" experience=""/>
    <Skill title="Git" imageUrl="/gitLogo.svg" experience=""/>
    <Skill title="XR" imageUrl="/xr-icon.svg" experience=""/>
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
  width: 100%;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  background: linear-gradient(90deg, var(--dark-purple) 0%, var(--dark-blue) 100%);
}

@media screen and (max-width: 900px) {
  section {
    height: 8rem;
  }
}


</style>