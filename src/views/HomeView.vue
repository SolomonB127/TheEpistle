<template>
  <main>
    <section id="Matthew">
      <div class="container">
        <div class="row">
          <div class="col">
            <div class="bibleText">
              <p class="passage">Give us this day <br> our daily bread, <span>Matt. 6:11</span></p>
            </div>
          </div>
        </div>
      </div>
    </section>

     <!-- About Author -->
     <!-- <div class="container">
      <div class="row">
        <div class="col">
          <section class="imgAuthor">
            <div class="author">
              <img src="pictures\alexandru-zdrobau-unsplash-2.jpg" alt="">
              <p class="selfIntro">HI! i'm Omotolani Ezra and it's sooo good to be on this journey with you <br>
              </p>
            </div>
          </section>
        </div>
      </div>
     </div> -->
  </main>
</template>

<script>

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
    font-size: 1.2rem;
    margin-top: 150px;
  }
  span{
   /* position: absolute;
   bottom: 170px; */
   font-style: oblique;
  }
  
  .author img{
    position: relative;
    left: 42%;
    width: 20%;
    border-radius: 70%;
  }
  .selfIntro{
    text-align: center;
  }

  @media all and (200px <= width <= 820px) {
    .bibleText{
      width: auto;
    }
}

</style>
