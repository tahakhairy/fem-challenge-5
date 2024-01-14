<template>
  <main id="main-articles">
    <div class="container">
      <div class="main-content">
        <div class="heading-news">
          <img
            src="../assets/images/image-web-3-desktop.jpg"
            class="img-desktop"
            alt="web3"
          />
          <img
            src="../assets/images/image-web-3-mobile.jpg"
            alt="web3"
            class="img-mobile"
          />
          <h1>The Bright Future of Web 3.0?</h1>
          <div class="heading-info">
            <p>
              We dive into the next evolution of the web that claims to put the
              power of the platforms back into the hands of the people. But is
              it really fulfilling its promise?
            </p>
            <span class="btn bg-primary">Read More</span>
          </div>
        </div>
        <aside class="aside-content">
          <div class="articles">
            <h2>New</h2>
            <div class="article">
              <h3>Hydrogen VS Electric Cars</h3>
              <p>Will hydrogen-fueled cars ever catch up to EVs?</p>
            </div>
            <hr />
            <div class="article">
              <h3>The Downsides of AI Artistry</h3>
              <p>
                What are the possible adverse effects of on-demand AI image
                generation?
              </p>
            </div>
            <hr />
            <div class="article">
              <h3>Is VC Funding Drying Up?</h3>
              <p>
                Private funding by VC firms is down 50% YOY. We take a look at
                what that means.
              </p>
            </div>
          </div>
        </aside>
      </div>
    </div>
  </main>

  <section id="top-headlines">
    <div class="container">
      <div class="top-headlines-content">
        <div class="headline">
          <img src="../assets/images/image-retro-pcs.jpg" alt="retro-pc" />
          <div class="headline-info">
            <h2>01</h2>
            <h4>Reviving Retro PCs</h4>
            <p>What happens when old PCs are given modern upgrades?</p>
          </div>
        </div>
        <div class="headline">
          <img src="../assets/images/image-top-laptops.jpg" alt="laptops" />
          <div class="headline-info">
            <h2>02</h2>
            <h4>Top 10 Laptops of 2022</h4>
            <p>Our best picks for various needs and budgets.</p>
          </div>
        </div>
        <div class="headline">
          <img
            src="../assets/images/image-gaming-growth.jpg"
            alt="gaming-growth"
          />
          <div class="headline-info">
            <h2>03</h2>
            <h4>The Growth of Gaming</h4>
            <p>How the pandemic has sparked fresh opportunities.</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup></script>

<style scoped>
#main-articles .main-content {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 1fr;
  padding: 1rem;
  gap: 2rem;
}

#main-articles .img-desktop {
  width: 100%;
}

.img-mobile {
  display: none;
}

#main-articles .heading-news {
  display: grid;
  grid-column: 1 / span 2;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
  align-items: start;
}

.heading-news .img-desktop {
  grid-column: 1 / span 2;
}

.heading-news h1 {
  font-size: 3.5rem;
  font-weight: 800;
  margin-right: 2rem;
  line-height: 1;
}

.heading-news .heading-info {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: start;
}
.heading-news .heading-info p {
  color: var(--dark-greyish-blue);
}
.heading-news .heading-info .btn {
  padding: 1rem 2rem;
  text-transform: uppercase;
  font-weight: bold;
  letter-spacing: 4px;
  margin-top: 2rem;
}

.heading-news .heading-info .btn:hover {
  background-color: var(--dark-blue);
  cursor: pointer;
}

#main-articles .aside-content {
  background-color: var(--dark-blue);
  padding: 1.5rem 2rem;
}

.aside-content p,
.aside-content hr {
  color: var(--greyish-blue);
}

.aside-content h2 {
  font-size: 2rem;
  margin-bottom: 1.5rem;
  color: var(--secondary-color);
}

.aside-content h3 {
  color: var(--light-white);
  margin-bottom: 1rem;
}

.aside-content h3:hover {
  cursor: pointer;
  color: var(--secondary-color);
}

.aside-content .articles {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
}

.aside-content hr {
  margin: 1rem 0;
  border: none;
  height: 1px;
  background-color: var(--greyish-blue);
  opacity: 0.4;
}

/* Top Headlines */
#top-headlines .top-headlines-content {
  padding: 1rem;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
}

#top-headlines .headline {
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 1rem;
}

#top-headlines .headline img {
  width: 100%;
}

#top-headlines .headline .headline-info {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
}

#top-headlines .headline .headline-info h2 {
  color: var(--greyish-blue);
}

#top-headlines .headline .headline-info p {
  color: var(--dark-greyish-blue);
}

#top-headlines .headline-info h4 {
  color: var(--dark-blue);
}
#top-headlines .headline-info h4:hover {
  cursor: pointer;
  color: var(--primary-color);
}

@media (max-width: 600px) {
  #main-articles .main-content {
    display: flex;
    flex-direction: column;
    padding: 0;
    gap: 4rem;
  }

  #main-articles .heading-news {
    display: grid;
    grid-template-columns: 1fr;
    gap: 1rem;
    grid-template-rows: 1.5fr 0.5fr 0.5fr;
    align-items: start;
  }

  .img-desktop {
    display: none;
  }

  .heading-news .img-mobile {
    display: block;
    width: 100%;
    grid-column: 1;
  }

  .heading-news h1 {
    margin: 0;
    font-size: 3rem;
  }

  #top-headlines .top-headlines-content {
    grid-template-columns: 1fr;
    gap: 2rem;
    padding: 0;
    margin-bottom: 2rem;
  }
}
</style>
