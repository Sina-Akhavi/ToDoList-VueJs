<template>
  <form action="" style="margin-bottom: 3%">
    <label for="task" class="text-input-label">Task</label>
    <input type="text" id="task" placeholder="Add Task" class="style-input-one">

    <label for="date" class="text-input-label">Data & Time</label>
    <input type="text" id="date" placeholder="Add Day & Time" class="style-input-two">

    <div class="reminder-container">
      <label for="reminder" class="reminder-label">Set Reminder<input type="checkbox" id="reminder" style="margin-left: 10%;"/></label>
    </div>
    
    <button type="submit">Save Task</button>
  </form>
</template>

<script>
</script>

<style scoped>

label.text-input-label {
  display: block;
  margin-top: 1%;
  margin-bottom: 0.5%;
}

label.reminder-label {
  margin-left: -1%;
}

input.style-input-one {
  width: 100%;
  margin-bottom: 2%;
}

input.style-input-two {
  width: 100%;
  margin-bottom: 1%;
}


button {
  width: 100%;
  padding: 0.8%;
  background: black; 
  color: white;
  border-radius: 6px;
  font-weight: bold;
}

div.reminder-container {
  margin-bottom: 2%;
  padding: 1%;
}

</style>