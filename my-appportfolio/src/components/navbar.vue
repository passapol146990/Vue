<template>
  <div id="navbar">
    <img id="logo" src="./assets/ez.jpg">
    <a href="#contact">Contact</a>
    <a href="#news">about</a>
    <a href="#">Home</a>
  </div>
</template>

<script>
export default {
  name: "navbarVue",
};
/* When the user scrolls down, hide the navbar. When the user scrolls up, show the navbar */
var prevScrollpos = window.pageYOffset;
window.onscroll = function() {
  var currentScrollPos = window.pageYOffset;
  if (prevScrollpos > currentScrollPos) {
    document.getElementById("navbar").style.top = "0";
  } else {
    document.getElementById("navbar").style.top = "-50px";
  }
  prevScrollpos = currentScrollPos;
}
</script>

<style scoped>
#navbar {
  background-color: #333; /* Black background color */
  position: fixed; /* Make it stick/fixed */
  top: 0; /* Stay on top */
  width: 100%; /* Full width */
  left: 0;
  transition: top 0.3s; /* Transition effect when sliding down (and up) */
}

/* Style the navbar links */
#navbar a {
  float: right;
  display: block;
  color: white;
  text-align: center;
  padding: 15px;
  text-decoration: none;
}

#navbar a:hover {
  background-color: #ddd;
  color: black;
}

</style>
