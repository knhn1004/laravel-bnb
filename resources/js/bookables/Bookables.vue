<template>
  <div>
    <BookableListItem
      :title="bookable1.title"
      :content="bookable1.content"
      :price="1500"
    />
    <BookableListItem
      :title="bookable2.title"
      :content="bookable2.content"
      :price="1000"
    />
  </div>
</template>

<script>
import BookableListItem from './BookableListItem';

export default {
  components: {
    BookableListItem,
  },
  data() {
    return {
      bookable1: {
        title: 'Cheap Villa1!!!',
        content: 'a very cheap villa 1',
      },
      bookable2: {
        title: 'Cheap Villa2',
        content: 'a very cheap villa 2',
      },
    };
  },
  created() {
    setTimeout(() => {
      this.bookable1.title = 'Cheap Villa (updated)';
    }, 2000);
  },
  //beforeCreate() {
  //  console.log('before create');
  //},
  //created() {
  //  console.log('created');
  //},
  //beforeMount() {
  //  console.log('before mount');
  //},
  //mounted() {
  //  console.log('mounted');
  //},
  //beforeDestroy() {
  //  console.log('before destroy');
  //},
  //destroyed() {
  //  console.log('destroyed');
  //},
};
</script>
