<template>
  <div>
    <!-- Footer wrapper to contain the footer content -->
    <div class="footer-wrapper">
      <!-- Footer content container -->
      <div class="footer-content">
        <!-- Copyright text -->
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
  /* Center the content horizontally */
  display: flex;
  justify-content: center;
  /* Set background color */
  background-color: #fafafa;
  /* Add padding */
  padding: 1.5rem;
  /* Add margin to create some space from the content above */
  margin-top: 2rem;
}

.footer-content {
  /* Set the maximum width of the content */
  max-width: 800px;
}

h1 {
  /* Set font size */
  font-size: 0.9rem;
  /* Set text color */
  color: #8e8e8e;
  /* Remove margin to prevent any unwanted spacing */
  margin: 0;
}
</style>




