<script setup>
const props = defineProps({
  difficulty: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <p
    class="difficulty"
    :class="
      props.difficulty === 'easy'
        ? 'bg-green-700'
        : props.difficulty === 'medium'
        ? 'bg-yellow-500'
        : 'bg-red-600'
    "
  >
    {{ props.difficulty }}
  </p>
</template>

<style lang="postcss" scoped>
.difficulty {
  @apply absolute bottom-6 left-8 rounded-full px-4 py-2 font-bold capitalize text-slate-700 text-white;
}
</style>