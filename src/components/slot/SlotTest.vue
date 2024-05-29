<template>
  <div>
    <h3>당신이 경험한 프론트 엔드 기술은?(두번째:slot기본)</h3>
    <CheckBox2
      v-for="item in items"
      :key="item.id"
      :id="item.id"
      :checked="item.checked"
      @check-changed="CheckBoxChanged"
    >
      <span v-if="item.checked" style="color: blue; text-decoration: underline">
        <i>{{ item.label }} (slot) (checked)</i></span
      >
      <span v-else style="color: gray"
        >{{ item.label }} (slot) (unchecked)</span
      >
    </CheckBox2>
  </div>
</template>

<script>
import CheckBox2 from './CheckBox2.vue';

export default {
  name: 'SlotTest',
  components: { CheckBox2 },
  data() {
    return {
      items: [
        { id: 'V', checked: true, label: 'Vue' },
        { id: 'A', checked: false, label: 'Angular' },
        { id: 'R', checked: false, label: 'React' },
        { id: 'S', checked: false, label: 'Svelte' },
      ],
    };
  },
  methods: {
    CheckBoxChanged(data) {
      // e >> { id, checked: $event.target.checked }
      // {id, checked: $event.target.checked }

      let item = this.items.find((item) => item.id === data.id);
      item.checked = data.checked;
    },
  },
};
</script>
