<script setup></script>
<template>
  <nav>
    <div class="nav-container">
      <img
        src="/src/assets/hourlies_logo.png"
        alt="Hourlies"
        style="width: 100px"
      />
      <div class="nav-button-container">
        <RouterLink :to="{ name: 'home' }">
          <p class="nav-button">Home</p>
        </RouterLink>
        <RouterLink :to="{ name: 'home' }">
          <p class="nav-button">About</p>
        </RouterLink>
        <RouterLink :to="{ name: 'home' }">
          <p class="nav-button">Features</p>
        </RouterLink>
        <RouterLink :to="{ name: 'home' }">
          <p class="nav-button">Characters</p>
        </RouterLink>
        <RouterLink :to="{ name: 'home' }">
          <p class="nav-button">Notice</p>
        </RouterLink>
      </div>
    </div>
  </nav>
</template>
<style scoped>
nav {
  position: sticky;
  top: 0;
  background-color: rgb(30, 29, 43);
  padding: 15px;
  z-index: 2;
}
.nav-container {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  margin-left: 20px;
  margin-right: 20px;
}
.nav-button-container {
  display: flex;
  flex-direction: row;
  gap: 20px;
}
.nav-button {
  color: white;
}
</style>
