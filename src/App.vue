<template>
  <div class="center">
    <ul>
      <Profile name="CapoStudios" image="https://avatars.githubusercontent.com/u/94376641?s=400&u=2ef90995057f68bdb1a9315bd3a3183ccd341479&v=4"/>
      <Card name="GitHub" icon="fa fa-github" url="https://github.com/CapoStudios" margin="200px" media="188px"/>
      <Card name="Instagram" icon="fa fa-instagram" url="https://www.instagram.com/" margin="172px" media="164px"/>
      <Card name="Twitter" icon="fa fa-twitter" url="https://twitter.com/" margin="198px" media="185px"/>
      <Card name="Linkedin" icon="fa fa-linkedin" url="https://www.linkedin.com/" margin="187px" media="176px"/>
    </ul>
  </div>
</template>

<script>
import Card from "./components/Card.vue";
import Profile from "./components/Profile.vue";

export default {
  name: 'App',
  components: {
    Card,
    Profile,
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@500&display=swap');

html, body {
  font-family: 'Oswald', Helvetica, Arial, sans-serif;
  background-color: #191919;
}

#app {
  font-family: 'Oswald', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: #191919;
  color: #eee;
  margin-top: 40px;
}

.center {
  width: 400px;
  height: 500px;
  margin: 0 auto;
  border: 2px solid #eee;
  border-radius: 25px;
}

li {
  margin-top: 50px;
  width: 350px;
}

ul{
  list-style: none;
  display: block;
  justify-content: center;
  align-content: space-between;
  padding: 10px 0;
}

@media only screen and (max-width: 600px)  {
  #app {
    margin-top: 20px;
  }
  .center {
    height: 440px;
    width: 350px;
  }
  li {
    margin-top: 40px;
    width: 250px;
  }
  ul {
    padding: 10px 0;
  }
}
</style>