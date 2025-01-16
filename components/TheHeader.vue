<template>
  <header class="header">
    <div class="logoImage">
      <NuxtLink to="/mainPage">
        <img src="@/assets/image/food.png" class="logo" alt="Food Logo">
      </NuxtLink>
    </div>
    <nav class="menu">
      <ul class="menu-list">
        <li>
          <nuxt-link exact-active-class="active" to="/">Home</nuxt-link>
        </li>
        <li>
          <nuxt-link exact-active-class="active" to="/Contact">Contact US</nuxt-link>
        </li>
        <li>
          <nuxt-link exact-active-class="active" to="/my-team.vue">Team Info</nuxt-link>
        </li>
      </ul>
    </nav>
  </header>
</template>


<script>
export default {

}
</script>

<style scoped>
/* General Header Styling */
.header {
  background-color: #9aafc4;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10px 20px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  position: sticky;
  top: 0;
  z-index: 1000;
}

/* Logo Styling */
.logoImage img {
  max-height: 50px;
  width: auto;
}

/* Menu Styling */
.menu {
  display: flex;
  align-items: center;
}

.menu-list {
  list-style-type: none;
  display: flex;
  gap: 20px;
  margin: 0;
  padding: 0;
}

.menu-list li {
  font-size: 1rem;
}

.menu-list a {
  text-decoration: none;
  color: #333;
  font-weight: bold;
  transition: color 0.3s ease, border-bottom 0.3s ease;
}

.menu-list .active {
  color: #ff8c00; /* Highlight color for active link */
  border-bottom: 2px solid #ff8c00; /* Underline active link */
}

.menu-list a:hover {
  color: #ff8c00;
}

/* Mobile Responsiveness */
@media (max-width: 768px) {
  .header {
    flex-wrap: wrap;
    justify-content: center;
  }

  .menu-list {
    flex-direction: column;
    gap: 10px;
    text-align: center;
  }
}
</style>
