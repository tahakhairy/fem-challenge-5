<template>
  <nav id="main-nav">
    <div class="container">
      <div class="nav-content">
        <img src="../assets/images/logo.svg" alt="app-logo" />
        <ul class="nav-links">
          <li><a href="#">Home</a></li>
          <li><a href="#">New</a></li>
          <li><a href="#">Popular</a></li>
          <li><a href="#">Trending</a></li>
          <li><a href="#">Categories</a></li>
        </ul>

        <div class="nav-menu" @click="openModal"></div>
      </div>
    </div>
  </nav>
</template>

<script setup>
const emit = defineEmits(["openMenu"]);
const openModal = () => {
  emit("openMenu", true);
  document.body.classList.add("modal-open");
};
</script>

<style scoped>
#main-nav .nav-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

#main-nav img {
  padding-left: 1.2rem;
}

#main-nav .nav-links {
  list-style: none;
  display: flex;
}

#main-nav .nav-links li {
  padding: 1rem 1.3rem;
}

#main-nav .nav-links li a {
  color: var(--dark-greyish-blue);
  text-decoration: none;
}

#main-nav .nav-links li a:hover {
  color: var(--secondary-color);
}

.nav-menu {
  display: none;
}

@media (max-width: 600px) {
  #main-nav img {
    width: 15%;
    padding: 0;
  }
  .nav-links li {
    display: none;
  }

  .nav-menu {
    display: block;
    width: 50px;
    height: 4px;
    background-color: black;
    position: relative;
  }

  .nav-menu::before,
  .nav-menu::after {
    position: absolute;
    content: "";
    height: 4px;
    width: 50px;
    background-color: black;
  }

  .nav-menu::before {
    bottom: 8px;
  }
  .nav-menu::after {
    top: 8px;
  }

  .nav-menu:hover {
    cursor: pointer;
  }
}
</style>
