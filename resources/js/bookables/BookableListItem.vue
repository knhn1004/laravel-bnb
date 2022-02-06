<template>
  <div class="card">
    <div class="card-body">
      <h2 class="card-title h5">{{ title }}</h2>
      <p class="card-text">{{ content }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    content: String,
    price: Number,
  },
};
</script>
