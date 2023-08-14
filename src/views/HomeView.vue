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
          <section>
            <div class="worries">
              <img src="pictures\La microbiota en las adicciones.jpg" alt="" width="300">
              <h3>WHEN YOU (& YOUR PEOPLE) ARE <br> TROUBLED WHO DO YOU LOOK ONTO</h3>
              <h3 class="read">
                <RouterLink to="/diary">
                  READ <span>&raquo;</span>
                </RouterLink>
              </h3>
            </div>

            <div class="worries">
              <img src="pictures\La microbiota en las adicciones.jpg" alt="" width="300">
              <h3>WHEN YOU (& YOUR PEOPLE) ARE <br> TROUBLED WHO DO YOU LOOK ONTO</h3>
              <h3 class="read">
                <RouterLink to="/diary">
                  READ <span>&raquo;</span>
                </RouterLink>
              </h3>
            </div>

            <div class="worries">
              <img src="pictures\La microbiota en las adicciones.jpg" alt="" width="300">
              <h3>WHEN YOU (& YOUR PEOPLE) ARE <br> TROUBLED WHO DO YOU LOOK ONTO</h3>
              <h3 class="read">
                <RouterLink to="/diary">
                  READ <span>&raquo;</span>
                </RouterLink>
              </h3>
            </div>

            <div class="worries">
              <img src="pictures\La microbiota en las adicciones.jpg" alt="" width="300">
              <h3>WHEN YOU (& YOUR PEOPLE) ARE <br> TROUBLED WHO DO YOU LOOK ONTO</h3>
              <h3 class="read">
                <RouterLink to="/diary">
                  READ <span>&raquo;</span>
                </RouterLink>
              </h3>
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
  .worries{
    text-align: center;
    margin: 20px;
    border: 1px solid #ccc;
    border-radius: 10px;
    box-shadow: 10px 10px 6px  rgb(77, 68, 68);
    display: inline-block;
    background-color: burlywood;
}
  .worries h3{
    font-size: 1rem;
    font-weight: bold;
  }
  .worries span{
    display: none;
  }
  .worries:hover span{
    display: inline-block;
  }
  .read a{
    font-size: 1rem;
    font-weight: bold;
    text-decoration: underline;
    color: #000;
  }
  @media all and (200px <= width <= 700px) {
    .author img{
    margin-left: 25%;
  }
}

</style>
