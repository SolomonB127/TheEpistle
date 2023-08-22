<template>
  <main>
    <!-- Page Cover -->
    <section id="Matthew">
      <div class="container">
        <div class="row">
          <div class="col">
            <div class="bibleText">
              <p class="passage">Give us this day <br> our daily bread, <span>Matt. 6:11.</span></p>
            </div>
          </div>
        </div>
      </div>
    </section>

     <!-- About Author -->
     <div class="container">
      <div class="row">
        <div class="col">
          <section class="imgAuthor">
            <div class="author">
              <div class="centerContents">
                <img src="pictures\ann-voskamp.jpg" alt="" width="200">
                <p class="selfIntro"> <RouterLink to="/about">
                  HI! i'm Omotolani Ezra and it's sooo good to be on this journey with you... <br> something else
                  </RouterLink>
                </p>
              </div>
            </div>
          </section>
        </div>
      </div>
     </div>

     <!-- Main Content -->
     <div class="container">
      <div class="row">
        <div class="col">
          <section id="entriesCard">
            <div  class="entriesCard">
              <div class="f-row">
                <div class="entriesImgs">
                  <h2>
                      WHEN YOU &amp; (YOUR PEOPLE)  <br> ARE IN TROUBLE WHO DO  <br> YOU LOOK ONTO <br>
                      <RouterLink to="/Troubles">Read <span>&raquo;</span></RouterLink>
                  </h2>
                </div>

                <div class="entriesImgs" id="img-2">
                  <h2>
                     "... DO NOT BE AFRAID FOR JOY COMETH IN THE MORNING." <br>
                      <RouterLink to="/Troubles">Read <span>&raquo;</span></RouterLink>
                  </h2>
                </div>

                <div class="entriesImgs" id="img-3">
                  <h2>
                      WHEN YOU &amp; (YOUR PEOPLE)  <br> ARE IN TROUBLE WHO DO  <br> YOU LOOK ONTO <br>
                      <RouterLink to="/Troubles">Read <span>&raquo;</span></RouterLink>
                  </h2>
                </div>
              </div> 

              <!-- Second row -->
              <div class="s-row">
                <div class="entriesImgs" id="img-4">
                  <h2>
                      WHEN YOU &amp; (YOUR PEOPLE)  <br> ARE IN TROUBLE WHO DO  <br> YOU LOOK ONTO <br>
                      <RouterLink to="/Troubles">Read <span>&raquo;</span></RouterLink>
                  </h2>
                </div>

                <div class="entriesImgs" id="img-5">
                  <h2>
                     "... DO NOT BE AFRAID FOR JOY COMETH IN THE MORNING." <br>
                      <RouterLink to="/Troubles">Read <span>&raquo;</span></RouterLink>
                  </h2>
                </div>

                <div class="entriesImgs" id="img-6">
                  <h2>
                      WHEN YOU &amp; (YOUR PEOPLE)  <br> ARE IN TROUBLE WHO DO  <br> YOU LOOK ONTO <br>
                      <RouterLink to="/Troubles">Read <span>&raquo;</span></RouterLink>
                  </h2>
                </div>
              </div> 

              <!-- Third row -->
              <div class="t-row">
                <div class="entriesImgs" id="img-7">
                  <h2>
                      WHEN YOU &amp; (YOUR PEOPLE)  <br> ARE IN TROUBLE WHO DO  <br> YOU LOOK ONTO <br>
                      <RouterLink to="/Troubles">Read <span>&raquo;</span></RouterLink>
                  </h2>
                </div>

                <div class="entriesImgs" id="img-8">
                  <h2>
                     "... DO NOT BE AFRAID FOR JOY COMETH IN THE MORNING." <br>
                      <RouterLink to="/Troubles">Read <span>&raquo;</span></RouterLink>
                  </h2>
                </div>

                <div class="entriesImgs" id="img-9">
                  <h2>
                      WHEN YOU &amp; (YOUR PEOPLE)  <br> ARE IN TROUBLE WHO DO  <br> YOU LOOK ONTO <br>
                      <RouterLink to="/Troubles">Read <span>&raquo;</span></RouterLink>
                  </h2>
                </div>
              </div> 
            </div>
            <div class="more">
                <button>
                  <RouterLink to="/entries">
                    More posts
                  </RouterLink>
                </button>
            </div>
          </section>
        </div>
      </div>
     </div>

     <div class="container">
      <div class="row">
        <div class="col">
          <section id="quote">
            <div class="quote">
              <hr>
              <p>
                It is the Lord who goes before you. He will be with you; he will not leave you or forsake you. Do not fear or be dismayed.
                <i style="text-decoration: underline;">Courtesy of Deuteronomy 31:8 ESV.</i>
              </p>
            </div>
          </section>
        </div>
      </div>
     </div>
  </main>
  <RouterView />
</template>

<script>
  import { RouterLink, RouterView } from 'vue-router';
</script>

<style scoped>
  main{
    margin-top: 30px;
    overflow-x: hidden;
  }
  #Matthew{
    background-image: url(pictures/landscape.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    height: 600px;
    text-align: center;
  }

  .passage{
    font-weight: bold;
    font-style: italic;
    font-size: 1.9rem;
    margin-top: 200px;
    text-shadow: 20px 20px 5px #000;
    color: #f0f8ff;
  }
  span{
   font-style: oblique;
  }
  .centerContents {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center; /* Center-align the text */
  height: 60vh;
}
.author img {
  margin-bottom: 10px; 
  border-radius: 100%;
  border: 3px solid #000;
}

  .selfIntro{
    text-align: center;
  }
  .selfIntro a{
    color: #000;
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    font-weight: bold;
    text-decoration: none;
  }
  /* Main Contents */
  /* .entriesCard */
 .entriesImgs{
  background-image: url(pictures/WorriedImg.jpg);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  width: 100%;
  max-width: 330px;
  margin: 0 auto;
  height: 500px;
  border-radius: 20px;
  box-shadow: 10px 10px 5px gray;
  text-align: center;
  opacity: 0.65;
  cursor: pointer;
 }
 #img-2 {
  background-image: url(pictures/SunriseImg.jpg);
 }
.entriesImgs h2{
  margin-top: 250px;
  color: #000;
  font-weight: bolder;
}

.entriesImgs h2 a{
  color: #000;
  text-decoration: none;
  font-weight: bolder;
}
.entriesImgs h2 a span{
  display: none;
}
.entriesImgs h2 a:hover span{
  display: inline-block;
  font-weight: bolder;
}
 .entriesImgs:hover{
  position: relative;
  transition: .6s;
  opacity: 1;
  bottom: 15px;
}
.f-row {
  display: flex;
  justify-content: space-evenly;
  margin-bottom: 40px;
}
.s-row {
  display: flex;
  justify-content: space-evenly;
  margin-bottom: 40px;
}
.t-row {
  display: flex;
  justify-content: space-evenly;
}
.more{
  text-align: center;
  margin-top: 40px;
}
.more a{
  color: #000;
  text-decoration: none;
  font-weight: bolder;
}
.more a:hover{
  text-decoration: underline;
  transition: 0.8s ease-in;
  color: #f0f8ff;
}
.more button{
 border-radius: 20px;
 width: auto;
}
.more button:hover{
  background-color: #000;
}

/* Quotes */
#quote{
  margin-top: 40px;
}
.quote{
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}
.quote p{
  font-family: cursive;
  font-weight: bolder;
  font-size: 1.1rem;
  margin-left: 50px;
}
.quote hr{
  background-color: brown;
  height: 2px;
  width: 30%;
}

  @media all and (200px <= width <= 1024px) {
    
    .entriesImgs{
      margin-top: 40px;
      opacity: 1;
    }
    
    
    .entriesImgs{
      margin-top: 40px;
    }
  /* entriesCard */
  .f-row{
      flex-wrap: wrap;
    }
    .s-row{
      flex-wrap: wrap;
    }
    .t-row{
      flex-wrap: wrap;
    }
}
/* Qoutes */
@media screen and (200px <= width <= 799px) {
.quote hr{
  display: none;
}
.quote p{
  align-items: center;
}
}


</style>
