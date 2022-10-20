<template>
  <section>
    <span class="titleText">Want to work together ?</span>
    <span class="subText">If you want to see your vision become reality contact me at <u>norbert.vladika@gmail.com</u>.</span>
  </section>
</template>

<script>
export default {
  name: "Contact"
}
</script>

<style scoped>
section {
  padding-left: 9rem;
  padding-top: 7rem;
  color: black;
  height: 50rem;
  background: linear-gradient(90deg, var(--turquoise) 0%, var(--dark-purple) 100%);
}

section span {
  min-width: 40rem;
}

.titleText {
  max-width: 30%;
  display: block;
  font-size: 5rem;
  line-height: 7rem;
  font-weight: 700;
  letter-spacing: 0.03rem;
  margin-bottom: 4.4rem;
}

.subText {
  display: block;
  max-width: 30%;
  font-weight: 400;
  font-size: 3rem;
  line-height: 4rem;
}

@media screen and (max-width: 900px) {
  section {
    padding-left: 1rem;
    padding-top: 7rem;
    color: black;
    height: 50rem;
    background: linear-gradient(90deg, var(--turquoise) 0%, var(--dark-purple) 100%);
  }

  section span {
    min-width: 90%;
  }
}
</style>