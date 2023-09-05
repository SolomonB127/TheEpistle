<script >
import { RouterLink, RouterView } from 'vue-router';
import CareCategory from './components/SearchSuggestions/CareCategory.vue'

export default{
  data(){
    return{
      isSearchOpen: false,
      isOpen: false,
      email: '',
      error: '',
      isSubscribed: false,
      searchQuery: '',
      suggestedCategories: [], 
      showSuggestions: false,
    };
  },
  methods: {
    Opensearch(){
      this.isSearchOpen = !this.isSearchOpen;
      if (!this.isSearchOpen) {
        this.showSuggestions = false;
      }
    },
    openNav(){
      this.isOpen = true;
    },
    closeNav(){
      this.isOpen = false;
    },
    subscribe() {
      if (this.email.trim() === '') {
        this.error = 'Please enter a valid email.';
        return;
      }
      
    const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    if (!emailRegex.test(this.email)) {
      this.error = 'Please enter a valid email.';
      return;
    }

      this.isSubscribed = true;
      this.email = ''; 
      this.error = '';
    },
    updateSuggestions() {
      this.suggestedCategories = [].filter(category =>
        category.toLowerCase().includes(this.searchQuery.toLowerCase())
      );
    },
    navigateToCategory(category) {
    this.showSuggestions = false;
    this.$router.push(`/category/${category}`);
  },
  },
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
              <RouterLink to="/entries">DiaryEntries</RouterLink>
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
              <RouterLink to="/entries">DiaryEntries</RouterLink>
            </li>
            <li>
              <RouterLink to="/contact">Contact</RouterLink>
            </li>
          </ul>

          <ul>
            <li>
              <img alt="" class="Sbtn" src="pictures\icons8-search-150.png" @click="Opensearch" width="30">
              <img/>
            </li>
              <!-- <img alt="" id="dark" v-if="isDarkTheme" src="pictures\icons8-sun-24.png" @click="toggleTheme">
              <img
                v-else
                src="pictures\icons8-dark-24.png"
                alt=""
                id="dark"
                @click="toggleTheme"
              />
            </li> -->
          </ul>
        </nav> 
    </header>
    <span>
      <input type="search" id="search" placeholder="Search Here..." autofocus="off" v-show="isSearchOpen" v-model="searchQuery" @input="updateSuggestions" @focus="showSuggestions = true">
      <div id="suggetions" class="suggestions" v-if="showSuggestions">
        <h3>Suggested Searches</h3>
        <ul>
          <li>
            <RouterLink to="/Troubles">TROUBLES</RouterLink>
          </li>
          <li>
            <RouterLink to="/Troubles">PEACE</RouterLink>
          </li>
          <li>
            <RouterLink to="/Troubles">CARE</RouterLink>
          </li>
        </ul>
        <ul >
          <li>
            <RouterLink to="/Trouble">TROUBLES</RouterLink>
          </li>
          <li>
            <RouterLink to="/Peace">PEACE</RouterLink>
          </li>
          <li>
            <RouterLink to="/Cares">CARE</RouterLink>
          </li>
        </ul>
        <ul >
          <li>
            <RouterLink to="/Fear">FEARS</RouterLink>
          </li>
          <li>
            <RouterLink to="/Doubts">DOUBTS</RouterLink>
          </li>
          <li>
            <RouterLink to="/Troubles">CARE</RouterLink>
          </li>
        </ul>
      </div>
    </span>

    <!-- Search Suggestions Components -->
    <CareCategory />
    
    <RouterView />
   
  <!-- Footer -->
  <footer>
    <div class="container-fluid">
      <div class="row">
        <div class="col">
          <section id="footer">
            <h2>
              Stay In Touch.
            </h2>
            <div class="footer">
              <p>Subscribe to stay notified.</p>
              <p><input type="email" v-model="email" name="subscribe" class="sub-box" placeholder="Enter e-mail..." autofocus="off"></p>
              <button id="sub-btn" class="sub-btn" @click="subscribe">Subscribe</button>
              <p v-if="error" class="error-msg">{{ error }}</p>
              <p v-if="isSubscribed" class="success-msg">Thank you for subscribing!</p>
            </div>
            <div id="social">
              <div>
                <RouterLink to="https://www.facebook.com"><img src="pictures\icons8-facebook-120.png" alt="facebook" width="50"></RouterLink>
              </div>
              <div>
                <RouterLink to="https://www.pinterest.com"><img src="pictures\icons8-pinterest-120.png" alt="pinterest" width="50"></RouterLink>
              </div>
              <div>
                <RouterLink to="https://www.instagram.com"><img src="pictures\icons8-instagram-120.png" alt="instagram" width="50"></RouterLink>
              </div>
            </div>
            <section id="rights">&copy;copyright 2023.</section>
          </section>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped>
*{
  margin: 0;
  padding: 0;
  list-style-type: none;
}
/* Header Section */
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
.Sbtn{
  margin-right: 20px;
  cursor: pointer;
}
 #search{
 width: 100%;
 height: 40px;
 font-family: 'Times New Roman', Times, serif;
 }
 /* suggested searches */
 .suggestions h3{
  text-align: center;
 }
 .suggestions ul{
  display: flex;
  justify-content: space-evenly;
  margin-top: 20px;
 }
 .suggestions{
  font-size: 1.2rem;
  width: 100%;
  background-color: #6e6b6b;
 }
 .suggestions a{
  color: #fff;
  text-decoration: none;
  font-family: 'Times New Roman', Times, serif;
 }
 .suggestions a:hover{
  text-decoration: underline;
 }
 #mainSidenav{
  display: none;
 }


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

@media all and (801px <= width <= 1024px){
    body{
      overflow-x: hidden;
    }
   
 nav li{
  display: inline;
  margin: 0 1rem;
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
}

/* Footer Section */
#footer{
  width: 100%;
  height: fit-content;
  background-color: gray;
  text-align: center;
  color: #fff;
}
#footer h2{
  padding-top: 20px;
}
.footer{
  padding-top: 30px;
}
.footer p{
  font-size: 1.1rem;
  font-weight: 600;
  /* font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif; */
}
#sub-btn{
    font-size: 1rem;
    /* font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif  ; */
    width: 20%;
    height: 30px;
    background-color: black;
    color: #fff;
    border: none;
    margin-top: 10px;
}
.sub-box{
    width: 20%;
    height: 25px;
    outline: none;
    margin-top: 20px;
    font-size: 1rem;
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}
#social{
    display: flex;
    justify-content: center; 
}
#rights{
    text-align: center;
    margin-top: 30px;
    font-size: 1.25rem;
    font-weight: bolder;
}
/* Error handling */
.error-msg {
  color: red;
}
.success-msg {
  color: green;
}
/* Subscription */
@media all and (200px <= width <= 1024px) {
    #sub-btn{
        width: 30%; 
    }
    .sub-box{
        width: auto;
    }
}

</style>
