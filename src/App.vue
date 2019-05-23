<template>
  <div id="app">
    <!-- Bootstrap responsive navbar - collapses to hamburger menu -->
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <a class="navbar-brand" href="index.html">Make It Sewstainable</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        <div class="navbar-nav">
          <a class="nav-item nav-link" href="index.html">Home</a>
          <a class="nav-item nav-link" href="gallery.html">Gallery</a>
          <a class="nav-item nav-link" href="#">Blog</a>
          <a class="nav-item nav-link" href="faq.html">FAQ</a>
        </div>
      </div>
    </nav>
    <!-- Hero image at top of page -->
      <header class="hero-image">
        <div class="hero-text">
          <h1>Make It Sewstainable</h1>
          <!-- Button with color/scale transition -->
          <button v-on:click="newbie = !newbie" class="hero-button">I'm new here</button>
          <button v-on:click="returning = !returning" class="hero-button">I've been here before</button>
        </div>
      </header>
      <main>
        <!-- Using v-if to show this content if this button is clicked -->
        <article v-if="newbie">
          <h1>What is Sustainable Sewing?</h1>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
            aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit
            in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
            Excepteur sint occaecat cupidatat non proident, sunt in culpa qui
            officia deserunt mollit anim id est laborum.
          </p>
          <div class="container">
            <div class="row">
              <div class="col">
                <img src="/src/assets/gallery1.jpg" alt="tote bag" class="img-thumbnail" data-toggle="tooltip" title="Learn how to make this">
                <div class="caption">
                  <h3>Sourcing Sustainable Materials</h3>
                  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
                    eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
                </div>
              </div>
              <div class="col">
                <img src="/src/assets/gallery2.jpg" alt="knit hat" class="img-thumbnail" data-toggle="tooltip" title="Discover new crochet techniques">
                <div class="caption">
                  <h3>Projects for Fabric Scraps</h3>
                  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
                    eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
                </div>
              </div>
              <div class="col">
                <img src="/src/assets/gallery3.jpg" alt="quilt" class="img-thumbnail" data-toggle="tooltip" title="Click for tutorial">
                <div class="caption">
                  <h3>Sewing for a Good Cause</h3>
                  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
                    eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
                </div>
              </div>
            </div>
          </div>
          <h2>How Can I get Involved?</h2>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
            aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit
            in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
            Excepteur sint occaecat cupidatat non proident, sunt in culpa qui
            officia deserunt mollit anim id est laborum.
          </p>
        </article>
        <!-- Using else-if to show this content only if this button is clicked -->
        <article v-else-if="returning">
          <h1>What's New in the Community</h1>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
            aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit
            in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
            Excepteur sint occaecat cupidatat non proident, sunt in culpa qui
            officia deserunt mollit anim id est laborum.
          </p>
          <div class="container">
            <div class="row">
              <div class="col">
                <img src="/src/assets/yarn.jpg" alt="yarn" class="img-thumbnail">
                <div class="caption">
                  <h3>Choosing Eco-Yarn</h3>
                  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
                    eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
                </div>
              </div>
              <div class="col">
                <img src="/src/assets/sewing-machine.jpg" alt="quilting" class="img-thumbnail">
                <div class="caption">
                  <h3>Quilting Your Scraps</h3>
                  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
                    eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
                </div>
              </div>
              <div class="col">
                <img src="/src/assets/singer.jpg" alt="sewing machine" class="img-thumbnail">
                <div class="caption">
                  <h3>Prolong the Life of Your Machine</h3>
                  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
                    eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
                </div>
              </div>
            </div>
          </div>
        </article>
     </main>
  </div>
</template>

<script>
// Setting boolean values for if/else variables
export default {
  name: 'app',
  data () {
    return {
      newbie: false,
      returning: false,
    }
  }
}
</script>

<style lang="scss">

* {
  box-sizing: border-box;
}

body, html {
  height: 100%;
  max-width: 100%;
  overflow-x: hidden;
  margin: 0;
}

// Page styles for main text
main {
  font-family: Helvetica, sans-serif;
  font-size: 1em;
  margin: 2em;
  & h1 {
    font-size: 2em;
  }
  & h2 {
    font-size: 1.75em;
  }
  & h3 {
    font-size: 1.5em;
  }
}
// Styling for main hero image
.hero-image {
  background-image: url('/src/assets/header.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  position: relative;
  height: 500px;
  width: 100%;
}

// Text laying over hero image
.hero-text {
    text-align: center;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: white;
}

// Mixin for transitions
@mixin transition($what: all, $time: 0.2s, $how: ease-in-out) {
  -webkit-transition: $what $time $how;
  -moz-transition:    $what $time $how;
  -ms-transition:     $what $time $how;
  -o-transition:      $what $time $how;
  transition:         $what $time $how;
}
// Styling for button in page hero
.hero-button {
  display: inline-block;
  @include transition(all,0.5s,ease-in-out);
  width: 45%;
  font-size: 1.2em;
  font-weight: bold;
  font-family: Raleway, sans-serif;
  text-decoration: none;
  text-align: center;
  color: white;
  background-color: rgba(224, 98, 133, 0.9);
  padding: 4px 30px 4px 30px;
  margin: 10px;
  border: none;
  border-radius: 8px;
  &:hover {
    background-color: darken(rgba(224, 98, 133, 0.9), 10%);
    cursor: pointer;
    transform: scale(1.05);
  }
}
// Styling for the hero h1
header h1 {
  font-family: Helvetica, sans-serif;
  font-size: 4em;
  font-weight: bold;
  text-transform: uppercase;
  text-shadow: 2px 2px black;
}
// Adding some spacing between images and following paragraph
.img-thumbnail {
  margin-bottom: 1rem;
}

.caption p {
  font-size: 0.75em;
  margin-bottom: 2rem;
}
</style>
