<template>
  <div @dblclick="$emit('toggle-reminder', task.id)">
    <i class="fas fa-times" @click="$emit('delete-task', task.id)"></i>
    <h3>
      {{ task.text }}
    </h3>
    <p>{{ task.date }}</p>
  </div>
</template> 

<script>
export default {
  props: ['task'],
  emits: ['delete-task', 'toggle-reminder'],
  methods: {
    
  }
}
</script>


<style scoped>
  div {
    padding-left: 0%;
  }

  i {
    float: right;
    color: red;
    cursor: pointer;
  }

</style>