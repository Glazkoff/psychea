<template>
  <div>
    <div id="nav">
      <router-link to="/">Главная</router-link>
      <router-link to="/test">Тестирование</router-link>
      <router-link to="/result">Результат</router-link>
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
#nav * {
  display: block;
  padding: 16px;
  text-decoration: none;
  color: #fff;
  font-size: 1.1rem;
}
#nav *:not(:last-child) {
  border-right: 2px solid rgba(255, 255, 255, 0.2);
}
</style>