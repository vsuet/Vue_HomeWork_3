<template>
  <div>
    <p>Введите ваше имя:</p>
    <input type="text" v-model="newName" />
    <p>Выберите, какие языки программирования вы знаете:
      <input type="checkbox" id="cpp" value="C++" v-model="newSkill">
      <label for="cpp">C++</label>
      <input type="checkbox" id="js" value="JavaScript" v-model="newSkill">
      <label for="js">JavaScript</label>
      <input type="checkbox" id="py" value="Python" v-model="newSkill">
      <label for="py">Python</label>
    </p>
    <button @click="names.push(newName), skills.push(newSkill)">Добавить</button>
  </div>
</template>

<script>

export default {
  name: "formVue",
  props: ['names', 'newName', 'skills', 'newSkill']
}
</script>

<style scoped>

</style>