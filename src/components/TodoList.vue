<template>
  <div class="todo-list">
    <div v-for="(todo, index) in todos" :key="index" class="todo-item">
      {{ todo.description }}
      <Button icon="pi pi-pencil" class="p-button-rounded p-buton-text" />
      <Button icon="pi pi-trash" class="p-button-rounded p-buton-text" />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    todos: Array
  }
};
</script>

<style scope>
.todo-list {
  margin: 1rem;
}
.todo-item {
  display: flex;
  align-items: center;
  border-bottom: 1px solid lightgray;
}
</style>
