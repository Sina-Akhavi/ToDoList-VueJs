
<template>
  <div class="border-style">
    <Header></Header>
    <TaskForm/>
    <Tasks :tasksArray="tasks" @toggle-reminder="toggleReminder" @delete-task="deleteTask" />

  </div>
</template>

<script>
import Header from './components/Header.vue'
import Tasks from './components/Tasks.vue'
import TaskForm from './components/TaskForm.vue'

export default {
  name: 'App',
  components: {
    Header,
    Tasks,
    TaskForm
  },
  data() {
    return {
      tasks: [
        {
          id: 0,
          text: "study for your midterm",
          date: "On Saturday",
          reminder: false
        },
        {
          id: 1,
          text: "help your mother",
          date: "Today evening",
          reminder: true
        },
        {
          id: 2,
          text: "go shopping",
          date: "Tuesday 17:00",
          reminder: false
        },
      ]
    }
  },
  methods: {
    toggleReminder(id) {
      this.tasks.forEach(task => {
        task.reminder = task.id === id ? !task.reminder : task.reminder
      })
    },

    deleteTask(id) {
      this.tasks = this.tasks.filter((task) => 
        task.id !== id
      )
    }

  }
}
</script>

<style scoped>
.border-style {
  border: 2px solid rgb(168, 160, 160);
  width: 97%;
  height: 80%;
  position: relative;
  padding: 15px;
  border-radius: 8px;
}
</style>
