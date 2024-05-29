<template>
  <div>
    <InputName v-model:nickName="searchName" />
    <h3>검색어 : {{ searchName }}</h3>
  </div>
</template>

<script>
import InputName from './components/directive/InputName.vue';

export default {
  name: 'App',
  components: { InputName },
  data() {
    return { searchName: 'zzzzzzz' };
  },
  // methods: {
  //   changeSearchName(name) {
  //     console.log(name);
  //     this.searchName = name;
  //   },
  // },
};
</script>
