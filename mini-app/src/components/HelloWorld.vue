<template>
  <div class="hero-container">
    <h1>Get more done with our powerful to-do list app</h1>
    <p>Join millions of people around the world who use our app to stay organized and get things done.</p>
    <button>Get started for free</button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
};
</script>

<style scoped>
.hero-container {
  background-image: url("https://images.unsplash.com/photo-1529253796989-07a7d829fe1a?ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80");
  background-position: center;
  background-size: cover;
  height: 500px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

h1 {
  color: #000;
  font-size: 3rem;
  margin-bottom: 1rem;
}

p {
  color: #000;
  font-size: 1.5rem;
  margin-bottom: 2rem;
  max-width: 600px;
  line-height: 1.5;
}

button {
  background-color: #fff;
  color: #333;
  font-size: 1.2rem;
  padding: 1rem 2rem;
  border: none;
  border-radius: 3px;
  cursor: pointer;
  transition: all 0.3s ease;
}

button:hover {
  background-color: #333;
  color: #fff;
}
</style>
