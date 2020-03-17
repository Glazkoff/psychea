<template>
  <div>
    <div id="nav">
      <router-link to="/" active-class="nav-active" exact
        ><span>Главная</span></router-link
      >
      <router-link to="/test" active-class="nav-active" exact
        ><span>Тестирование</span></router-link
      >
      <router-link to="/result" active-class="nav-active" exact
        ><span>Результат</span></router-link
      >
    </div>
  </div>
</template>

<script>
export default {
  name: "Menu"
};
</script>

<style>
#nav {
  width: 100vw;
  display: flex;
  background: linear-gradient(90deg, #e66465, #9198e5);
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.2);
}
#nav a {
  display: block;
  padding: 16px;
  text-decoration: none;
  color: #fff;
  font-size: 1.1rem;
  font-family: "Roboto ";
}
#nav *:not(:last-child) {
  /* border-right: 2px solid rgba(255, 255, 255, 0.2); */
}
.nav-active {
  font-family: "Roboto";
  font-weight: bold;
  background: linear-gradient(90deg, rgba(0, 0, 0, 0.25), rgba(0, 0, 0, 0.1));
}
</style>
