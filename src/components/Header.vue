<template>
  <header>
    <h1>Tasks tracker</h1>
    <Button
      @btn-click="$emit('toggle-add-task')"
      :text="showAddTask ? 'Close': 'Add task' "
      :color="showAddTask ? 'red' : 'green' "
    />
  </header>
</template>

<script>
import Button from './Button'
export default {
  name: 'Header',
  props: {
    title: String,
    showAddTask: Boolean,
  },
  components: {
    Button,
  },

  created(){
    // console.log(title)
  }
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>