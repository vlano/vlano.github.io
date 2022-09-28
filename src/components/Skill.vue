<template>
  <div class="skill">
    <span>{{ experience }}</span>
    <div class="technology">
      <img :src="imageUrl">
      <span>{{ title }}</span>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  title: String,
  imageUrl: String,
  experience: String
})
</script>

<style scoped>
img {
  height: 76px;
  filter: grayscale(90%);
}

.skill {
  font-size: 1.25rem;
  font-weight: 700;
  color: var(--white);
  display: flex;
  flex-direction: column;
}

.skill span {
  font-size: 1.25rem;
  margin-left: auto;
  color: var(--white);
  opacity: 0.7;
}


.technology {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: row;
  font-size: 48px;
  gap: 1.75rem;
}

.technology span {
  color: var(--white);
  font-size: 3rem;
}
</style>