<template>
  <div class="header-container">
    <div class="logo-container">
      <img src="https://i.imgur.com/7DrxCz3.png" alt="CheckMate Logo" />
    </div>
    <div class="search-container">
      <input type="text" placeholder="Search" />
    </div>
    <div class="actions-container">
      <button><i class="far fa-compass"></i></button>
      <button><i class="far fa-heart"></i></button>
      <button><i class="far fa-user"></i></button>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppHeader",
};
</script>

<style scoped>
.header-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
  background-color: #fff;
  border-bottom: 1px solid #dbdbdb;
  position: sticky;
  top: 0;
  z-index: 100;
}

.logo-container img {
  height: 3rem;
}

.search-container input[type="text"] {
  background-color: #fafafa;
  border: 1px solid #dbdbdb;
  border-radius: 3px;
  font-size: 1rem;
  padding: 0.5rem;
  width: 200px;
}

.actions-container button {
  background-color: transparent;
  border: none;
  cursor: pointer;
  font-size: 1.5rem;
  margin-left: 1rem;
}

.actions-container button i {
  color: #262626;
}
</style>

