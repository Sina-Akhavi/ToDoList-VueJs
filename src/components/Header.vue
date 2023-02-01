<template>
	<div>
		<h2>Task Tracker</h2>
    <Button></Button>
	</div>
</template>

<script>
import Button from './Button.vue' 
export default {
	name: 'Header',
  components: {
    Button,
  }

}

</script>


<style>

h2 {
  display: inline-block;
  font-family:Arial, Helvetica, sans-serif;
}

</style>