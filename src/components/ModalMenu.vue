<template>
  <div class="modal" v-if="isOpen">
    <div class="side-menu">
      <div class="container">
        <div class="menu-content">
          <img
            @click="$emit('closeMenu', false)"
            src="../assets/images/icon-menu-close.svg"
            alt="close"
          />
          <ul class="nav-links">
            <li><a href="#">Home</a></li>
            <li><a href="#">New</a></li>
            <li><a href="#">Popular</a></li>
            <li><a href="#">Trending</a></li>
            <li><a href="#">Categories</a></li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps(["isOpen"]);
</script>

<style scoped>
@media (max-width: 600px) {
  .modal {
    position: absolute;
    height: 100%;
    width: 100%;
    top: 0;
    left: 0;
    z-index: 1;
    background-color: rgba(0, 0, 0, 0.404);
    overflow: hidden;
  }

  .side-menu {
    width: 70%;
    height: 100dvh;
    background-color: var(--light-white);
    position: absolute;
    right: 0px;
  }

  .nav-links {
    list-style: none;
    display: flex;
    flex-direction: column;
    margin-top: 4rem;
  }

  .nav-links li {
    padding: 1rem 1.3rem;
  }

  .nav-links li a {
    color: black;
    text-decoration: none;
  }

  .container .menu-content {
    display: flex;
    flex-direction: column;
  }

  .menu-content img {
    width: 25%;
    align-self: flex-end;
    padding: 1rem 1.3rem;
    cursor: pointer;
  }

  .nav-links li a:hover {
    color: var(--secondary-color);
  }
}
</style>
