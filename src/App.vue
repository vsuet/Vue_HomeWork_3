<template>
  <div id="app" class="tabs">
    <input type="radio" name="tab-btn" id="tab-btn-1" value="">
    <label for="tab-btn-1">Список</label>
    <input type="radio" name="tab-btn" id="tab-btn-2" value="" checked>
    <label for="tab-btn-2">Добавить</label>
    <div id="content-1"><list :names="names" :skills="skills"></list></div>
    <div id="content-2"><form-vue :newName="newName" :newSkill="newSkill" :names="names" :skills="skills"></form-vue></div>
  </div>
</template>

<script>
import formVue from './components/formVue.vue'
import List from "@/components/list";

export default {
  name: 'App',
  components: {
    List,
    formVue,
  },
  data() {
    return {
      names: [],
      skills: [],
      newName: '',
      newSkill:[]
    }
  }
}
</script>

<style>
#tab-btn-1:checked~#content-1,
#tab-btn-2:checked~#content-2 {
  display: block;
}
.tabs>div {
  display: none;
  padding: 10px 15px;
  font-size: 16px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
