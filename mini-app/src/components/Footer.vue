<template>
  <div>
    <div class="footer-wrapper">
      <div class="footer-content">
        <h1>© 2023 CheckMate. All Rights Reserved.</h1>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppFooter",
};
</script>

<style scoped>
.footer-wrapper {
  display: flex;
  justify-content: center;
  background-color: #fafafa;
  padding: 1.5rem;
  margin-top: 2rem;
}

.footer-content {
  max-width: 800px;
}

h1 {
  font-size: 0.9rem;
  color: #8e8e8e;
  margin: 0;
}
</style>
