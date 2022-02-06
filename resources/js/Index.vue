<template>
  <div>
    <nav class="navbar bg-white border-bottom navbar-light">
      <div class="container">
        <router-link class="navbar-brand mr-auto" :to="{ name: 'home' }"
          >LaravelBnb</router-link
        >
        <router-link class="btn nav-button" :to="{ name: 'second' }"
          >Second</router-link
        >
      </div>
    </nav>
    <div class="container my-4 px-4">
      <router-view></router-view>
    </div>
  </div>
</template>
