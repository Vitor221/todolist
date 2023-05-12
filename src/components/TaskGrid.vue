<template>
  <div class="task-grid">
    <template v-if="tasks.length">
        <Task v-for="(task, index) in tasks" :key="index" :task="task" @taskDeleted="$emit('taskDeleted', index)" @taskStateChanged="$emit('taskStateChanged', index)"/>
    </template>
    <p v-else class="to-task">Sua vida está em dia :)</p>
  </div>
</template>

<script>
import Task from './Task.vue'

export default {
    name: 'TaskGrid',
    components: {
        Task
    },
    props: {
        tasks: {
            type: Array,
            require: true,
        }
    }
}
</script>

<style scoped>
.task-grid {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}

.task {
    margin: 10px;
}

.no-task {
    font-size: 1.7rem;
}
</style>