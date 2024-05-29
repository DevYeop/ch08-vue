<template>
  <div>
    <Child1 />
    <Child2 />
    <Child3 />
  </div>
</template>

<script>
import Child1 from '@/components/scope-module-css/Child1.vue';
import Child2 from '@/components/scope-module-css/Child2.vue';
import Child3 from '@/components/scope-module-css/Child3.vue';

export default {
  name: 'App',
  components: { Child1, Child2, Child3 },
};
</script>
