<template>
  <div id="app">
    <Header />
    <main id="main">
      <transition name="bounce" mode="out-in">
        <router-view></router-view>
      </transition>
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";
export default {
  components: {
    Header,
    Footer,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins&display=swap");

* {
  box-sizing: border-box;
}

body {
  font-family: "Poppins", Avenir, Helvetica, Arial, sans-serif;
  color: #345;
  background: url("./assets/pattern.svg") repeat top;
  background-color: #f1f1f1;
}

body,
ul,
li,
h1,
h2,
p {
  padding: 0px;
  margin: 0px;
}

ul {
  list-style: none;
}

a {
  text-decoration: none;
  color: #345;
}

img {
  max-width: 100%;
  display: block;
}

.btn {
  display: block;
  padding: 10px 30px;
  background: #87f;
  border: none;
  border-radius: 4px;
  color: white;
  text-align: center;
  font-size: 1rem;
  box-shadow: 0px 4px 8px rgba(30, 60, 90, 0.15);
  transition: all 0.3s;
  font-family: "Poppins", Avenir, Helvetica, Arial, sans-serif;
  cursor: pointer;
}

.btn:hover {
  background: #65d;
  transform: scale(1.1);
}
#app {
  display: flex;
  min-height: 100vh;
  flex-direction: column;
}

#main {
  flex: 1;
}

label {
  margin-bottom: 5px;
}

input,
textarea {
  border-radius: 4px;
  border: 1px solid white;
  padding: 15px;
  box-shadow: 0 4px 8px rgba(30, 60, 90, 0.1);
  transition: all 0.3s;
  font-size: 1rem;
  font-family: "Poppins", Avenir, Helvetica, Arial, sans-serif;
  margin-bottom: 15px;
}

input:hover,
textarea:hover,
textarea:focus,
input:focus {
  outline: none;
  box-shadow: 0 6px 12px rgba(30, 60, 90, 0.2);
  border-color: #87f;
}

.bounce-enter-active {
  animation: bounce-in 1s;
}
.bounce-leave-active {
  animation: bounce-in 1s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.1);
  }
  100% {
    transform: scale(1);
  }
}
</style>
