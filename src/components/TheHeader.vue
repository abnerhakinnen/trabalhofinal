<template>
  <header>
    <nav>
      <router-link to="/" class="logo">GalileuBooks</router-link>
      <router-link class="btn btn-primary" to="/entrar">Entrar</router-link>
    </nav>
  </header>
</template>

<script>
export default {
      name: "TheHeader",
}

</script>

<style scoped>

nav {
  color: white;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 15px 20px;
  box-shadow: 0 2px 4px rgba(30, 60, 90, 0.1);
}

.logo {
  padding: 10px 0;
  color: orange;
  font-size: 22px;
  text-decoration: none;
}

.logo:hover {
  padding: 10px 0;
  color: rgb(0, 0, 0);
  font-size: 22px;
  -webkit-transform: scale(1.1);
    -moz-transform: scale(1.1);
    -o-transform: scale(1.1);
    -ms-transform: scale(1.1);
    transform: scale(1.1);
}

.btn-primary{
  background-color:rgb(0, 0, 0);
  border: none;
  }

.btn-primary:hover{
  background-color: orange;
}

.darkmod{
  position: absolute;
  right: 120px;
  width: 20px;
}
</style>

