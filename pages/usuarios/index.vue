<template>
  <div>
    <h1>Usuarios</h1>
    <span v-for="(user, index) in usuarios" :key="index">
      <ul>
        <li>{{ user.nome }}</li>
      </ul>
    </span>
  </div>
</template>

<script>
export default {
  name: "User",
  computed: {
    usuarios() {
      return this.$store.state.users.users;
      //store.state.modulo.array de objetos
    },
  },
  data() {
    return {
      dados: this.$store.state.users,
    };
  },
};
</script>
