<template>
  <div v-for="task in tasksArray" :class="{'reminder-sign': task.reminder}">
    <Task :task="task" @toggle-reminder="$emit('toggle-reminder', task.id)" 
      @delete-task="$emit('delete-task', task.id)"/>

  </div>
</template>

<script>

import Task from './Task.vue'

export default {
  name: 'Tasks',
  props: ['tasksArray'],
  components: {
    Task
  },

  emits: ['delete-task', 'toggle-reminder'],
  methods: {
    
  }
}
</script>

<style scoped>

div {
  background: rgb(230, 225, 225);
  padding: 10px;
  width: 98%;
  margin-top: 5px;
  border-radius: 6px;
  padding-left: 25px;

}

.reminder-sign {
  border-left: 5px solid green;
}

</style>