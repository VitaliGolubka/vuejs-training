<template>
  <div>Now you in home page {{ a }}</div>
  <div>
    <div>
    </div>
  </div>
  <button @click="handlePushClick">Push</button>
</template>

<script lang="ts">
import { defineComponent, ref, onMounted } from 'vue';

export default defineComponent({
  setup() {
    const a = ref(5);
    onMounted(() => {
      a.value = ++a.value;
    });
    const handlePushClick = () => {
      a.value = ++a.value;
    };
    return {
      a,
      handlePushClick,
    };
  },
});
</script>
