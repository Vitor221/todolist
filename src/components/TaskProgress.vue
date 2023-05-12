<template>
  <div class="tasks-progress">
    <span class="progress-value">{{ progress }}%</span>
    <div class="progress-bar"></div>
  </div>
</template>

<script>
export default {
    name: 'TaskProgress',
    props: {
        progress: {
            type: Number,
            default: 0
        }
    }
}
</script>

<style>

</style>