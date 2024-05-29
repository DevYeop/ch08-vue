<template>
  <input
    type="text"
    :value="nickName"
    @input="$emit('update:nickName', $event.target.value)"
  />
  <!-- zzzzzzz -->
</template>

<script>
export default {
  name: 'InputName',
  props: ['nickName'],
};
</script>
