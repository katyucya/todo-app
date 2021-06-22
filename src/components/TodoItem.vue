<template>
  <InputText v-model="description" />
  <div class="div-botoes">
    <Button @click="cancel" class="bnt-voltar">Voltar</Button>
    <Button @click="saveTodo">Salvar</Button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      description: ""
    };
  },
  methods: {
    cancel() {
      this.$emit("cancel");
    },
    saveTodo() {
      this.$emit("saveTodo", { description: this.description });
    }
  }
};
</script>

<style scoped>
.div-botoes {
  margin-top: 1rem;
}
.bnt-voltar {
  margin-right: 1rem;
}
</style>
