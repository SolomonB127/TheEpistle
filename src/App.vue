<script >
import { RouterLink, RouterView } from 'vue-router';

export default{
  data(){
    return{
      Sbtn : true,
      isOpen: false,
    };
  },
  methods: {
    openNav(){
      this.isOpen = true;
    },
    closeNav(){
      this.isOpen = false;
      this.$router.push('/');
    }
  }
}

</script>

<template>
  <!-- Head/Nav Section -->
  <header>
      <nav>
        <!-- Side nav -->
        <div id="mainSidenav">
          <span style="font-size: 30px; cursor: pointer" @click="openNav">&#9776;</span>
          <!-- Sidebar -->
          <div
            id="mySidenav"
            class="sidenav"
            :style="{ width: isOpen ? '250px' : '0' }"
          >
            <h3>The Epistle</h3>
            <a class="closebtn" @click="closeNav">&times;</a>
            <RouterLink to="/">Home</RouterLink>
            <RouterLink to="/about">About</RouterLink>
            <RouterLink to="/diary">Diary Entries</RouterLink>
            <RouterLink to="/contact">Contact</RouterLink>
          </div>
        </div>
        <h1>The Epistle</h1>
        <ul>
          <li>
            <RouterLink to="/">Home</RouterLink>
          </li>

          <li>
            <RouterLink to="/about">About</RouterLink>
          </li>
          <li>
            <RouterLink to="/diary">Diary Entries</RouterLink>
          </li>
          <li>
            <RouterLink to="/contact">Contact</RouterLink>
          </li>
        </ul>

        <ul>
          <li>
            <img src="pictures\icons8-dark-24.png" alt="" id="dark">
          </li>
          <li>
            <img src="pictures\icons8-search-150.png" alt=""  width="20" @click="Sbtn = !Sbtn" id="S-btn">
            
          </li>
        </ul>
      </nav> 
  </header>
  <span>
    <input type="text" name="" id="search" placeholder="Search Here..." :class="{button : Sbtn}">
  </span>

  <RouterView />
</template>

<style scoped>
*{
  margin: 0;
  padding: 0;
  list-style-type: none;
}
 header{
  /* position: sticky;
  top: 0; */
  width: 100%;
  height: auto;
  background-color: grey;
  color: #fff;
 }
 h1{
  font-family: cursive;
 }
 header nav{
  display: flex;
  justify-content: space-between;
  align-items: center;
 }
 nav li{
  display: inline;
  margin: 0 3em;
 }
 nav a{
  color: white;
  text-decoration: none;
  font-weight: bolder;
  font-style: italic;
 }
 #search{
 width: 100%;
 height: 40px;
 }
 #S-btn{
  cursor: pointer;
 }
 .button{
  display: none;
 }
 #mainSidenav{
  display: none;
 }

 /* @media screen and (max-width: 834px) {
  header{
  width: 100%;
  height: auto;
  background-color: grey;
  color: #fff;
 }
 h1{
  font-family: cursive;
 }
 header nav{
  display: flex;
  justify-content: space-between;
  align-items: center;
 }
 nav li{
  display: inline;
  margin: 0 3em;
 }
 nav a{
  color: white;
  text-decoration: none;
  font-weight: bolder;
  font-style: italic;
 }
 #search{
 width: 100%;
 height: 40px;
 }
} */

@media all and (200px <= width <= 800px) {
  header nav{
    flex-direction: initial;
  }

  h1{
  font-size: large;
 }
 nav li {
    display: inline;
    margin: 0.5em 0;
  }
  nav a{
  display: none;
 }

  #mainSidenav{
  display: initial;
 }
  .sidenav {
  height: 100%;
  width: 0;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  background-color: #111;
  overflow-x: hidden;
  transition: 0.5s;
  padding-top: 60px;
  border-radius: 10px;
}
.sidenav h3{
  color: #fff;
  font-family: cursive;
  text-align: center;
}
.sidenav a {
  padding: 8px 8px 8px 32px;
  text-decoration: none;
  font-size: 25px;
  color: #818181;
  text-align: center;
  display: block;
  transition: 0.3s;
}

.sidenav a:hover {
  color: #f1f1f1;
}

.sidenav .closebtn {
  position: absolute;
  top: 0;
  right: 25px;
  font-size: 36px;
  margin-left: 50px;
  cursor: pointer;
}
}

@media all and (max-width:820px){
    body{
      overflow-x: hidden;
    }
    .sidenav {
        height: 100%;
        width: 0;
        position: fixed;
        z-index: 1;
        top: 0;
        left: 0;
        background-color: #111;
        overflow-x: hidden;
        transition: 0.5s;
        padding-top: 60px;
    }
      
      .sidenav a {
        padding: 8px 8px 8px 32px;
        text-decoration: none;
        font-size: 25px;
        color: #818181;
        text-align: center;
        display: block;
        transition: 0.3s;
        text-align: center;
    }
      
      .sidenav a:hover {
        color: #f1f1f1;
    }
      
      .sidenav .closebtn {
        position: absolute;
        top: 0;
        right: 25px;
        font-size: 36px;
        margin-left: 50px;
      }
      .sidenav .closebtn:hover{
        text-decoration: none;
      }
}
</style>
