<template>
  <div>
    <NoSlotTest />
    <hr />
    <SlotTest />
    <hr />
    <NamedSlotTest />
    <hr />
    <ScopedSlotTest />
  </div>
</template>

<script>
import NoSlotTest from './components/slot/NoSlotTest.vue';
import SlotTest from './components/slot/SlotTest.vue';
import NamedSlotTest from './components/slot/NamedSlotTest.vue';
import ScopedSlotTest from './components/slot/ScopedSlotTest.vue';

export default {
  name: 'App',
  components: { NoSlotTest, SlotTest, NamedSlotTest, ScopedSlotTest },
};
</script>
