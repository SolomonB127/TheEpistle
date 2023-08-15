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
              <img src="pictures\ann-voskamp.jpg" alt="" width="200">
              <p class="selfIntro"> <RouterLink to="/about">
                HI! i'm Omotolani Ezra and it's sooo good to be on this journey with you... <br> something else
              </RouterLink>
              </p>
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
                <RouterLink to="/entries">
                  <img src="pictures\La microbiota en las adicciones.jpg" alt="" width="300">
                  <h3>WHEN YOU &amp; (YOUR PEOPLE) ARE IN TROUBLE WHO DO YOU LOOK ONTO.</h3>
                  <h4>Read <span>&raquo;</span></h4>
                </RouterLink>

                <RouterLink to="/entries" class="entries">
                  <img src="pictures\La microbiota en las adicciones.jpg" alt="" width="300">
                  <h3>WHEN YOU &amp; (YOUR PEOPLE) ARE IN TROUBLE WHO DO YOU LOOK ONTO.</h3>
                  <h4>Read <span>&raquo;</span></h4>
                </RouterLink>

                <RouterLink to="/entries" class="entries">
                  <img src="pictures\La microbiota en las adicciones.jpg" alt="" width="300">
                  <h3>WHEN YOU &amp; (YOUR PEOPLE) ARE IN TROUBLE WHO DO YOU LOOK ONTO.</h3>
                  <h4>Read <span>&raquo;</span></h4>
                </RouterLink>
              </div>

              <!-- Second-Row -->
              <div class="s-row">
                <RouterLink to="/entries">
                  <img src="pictures\La microbiota en las adicciones.jpg" alt="" width="300">
                  <h3>WHEN YOU &amp; (YOUR PEOPLE) ARE IN TROUBLE WHO DO YOU LOOK ONTO.</h3>
                  <h4>Read <span>&raquo;</span></h4>
                </RouterLink>

                <RouterLink to="/entries" class="entries">
                  <img src="pictures\La microbiota en las adicciones.jpg" alt="" width="300">
                  <h3>WHEN YOU & (YOUR PEOPLE) ARE IN TROUBLE WHO DO YOU LOOK ONTO.</h3>
                  <h4>Read <span>&raquo;</span></h4>
                </RouterLink>

                <RouterLink to="/entries" class="entries">
                  <img src="pictures\La microbiota en las adicciones.jpg" alt="" width="300">
                  <h3>WHEN YOU &amp; (YOUR PEOPLE) ARE IN TROUBLE WHO DO YOU LOOK ONTO.</h3>
                  <h4>Read <span>&raquo;</span></h4>
                </RouterLink>
              </div>

              <!-- Third-Row -->
              <div class="t-row">
                <RouterLink to="/entries">
                  <img src="pictures\La microbiota en las adicciones.jpg" alt="" width="300">
                  <h3>WHEN YOU &amp; (YOUR PEOPLE) ARE IN TROUBLE WHO DO YOU LOOK ONTO.</h3>
                  <h4>Read <span>&raquo;</span></h4>
                </RouterLink>

                <RouterLink to="/entries" class="entries">
                  <img src="pictures\La microbiota en las adicciones.jpg" alt="" width="300">
                  <h3>WHEN YOU &amp; (YOUR PEOPLE) ARE IN TROUBLE WHO DO YOU LOOK ONTO.</h3>
                  <h4>Read <span>&raquo;</span></h4>
                </RouterLink>

                <RouterLink to="/entries" class="entries">
                  <img src="pictures\La microbiota en las adicciones.jpg" alt="" width="300">
                  <h3>WHEN YOU &amp; (YOUR PEOPLE) ARE IN TROUBLE WHO DO YOU LOOK ONTO.</h3>
                  <h4>Read <span>&raquo;</span></h4>
                </RouterLink>
              </div>
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
  
  .author img{
    margin: 20px 40%;
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
  #entriesCard{
    width: 20%;
    margin: 40px 45%;
}
  .f-row{
    display: flex;
    justify-content: space-evenly;
  }
  .s-row{
    display: flex;
    justify-content: space-evenly;
    margin-top: 60px;
  }
  .t-row{
    display: flex;
    justify-content: space-evenly;
    margin-top: 60px;
  }
  .entriesCard a{
    margin-right: 40%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
    text-decoration: none;
    font-size: 1.9rem;
    color: #000;
    background-color: burlywood;
    border-radius: 20px;
    box-shadow: 10px 10px 10px #000;
  }
.entriesCard img{
    border-radius: 20px;
}

.entriesCard a h3{
  font-weight: bold;
}
.entriesCard a h4{
  font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
  font-style: italic;
  font-weight: bold;
}
  @media all and (200px <= width <= 820px) {
    .author img{
    margin-left: 25%;
  }

  /* entriesCard */
  .f-row{
      flex-wrap: wrap;
    }
  .entries{
    margin-top: 60px;
  }
    .s-row{
      flex-wrap: wrap;
    }
    .t-row{
      flex-wrap: wrap;
    }
}

</style>
