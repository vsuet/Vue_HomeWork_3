<template>
  <div>
    <div class="cols">
      <div>
        <p>Имя:</p>
        <p v-for="(name, index) in names" :key="name">{{ index + 1 }}) {{ name }}</p>
      </div>
      <div>
        <p>Языки:</p>
        <p v-for="skill in skills" :key="skill">{{ skill }}</p>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      checkSkill:[]
    }
  },
  name: "list",
  props:['names', 'skills'],
}
</script>

<style scoped>
  .cols {
    column-count: 2;
    column-gap: 4%;
  }
</style>