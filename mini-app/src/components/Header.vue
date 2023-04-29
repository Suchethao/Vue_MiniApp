<!--
This is the header component of the CheckMate app.
It consists of a logo, search bar, and user actions.
The logo is displayed in a separate div with the class "logo-container",
while the search bar is in "search-container".
The user actions, which are represented by icons, are displayed in "actions-container".

The CSS for this component uses flexbox to arrange the elements.
The header has a white background with a border at the bottom.
The logo is styled to be 3rem high.
The search bar has a light gray background with a border and rounded corners.
The user action icons have a font size of 1.5rem and a margin of 1rem.
-->

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

