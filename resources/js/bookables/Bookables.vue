<template>
  <div>
    <BookableListItem
      v-if="bookable1"
      :title="bookable1.title"
      :content="bookable1.content"
      :price="1500"
    />
    <BookableListItem
      v-if="bookable2"
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
      bookable1: null,
      bookable2: null,
    };
  },
  created() {
    setTimeout(() => {
      this.bookable1 = {
        title: 'Cheap Villa 1',
        content: 'a very cheap villa 1',
      };
      this.bookable2 = {
        title: 'Cheap Villa 2',
        content: 'a very cheap villa 2',
      };
      //this.bookable3 = {
      //  title: 'Cheap Villa 3',
      //  content: 'a very cheap villa 3',
      //};
    }, 2000);

    //setTimeout(() => {
    //  console.log('first change');
    //  this.bookable1.title = 'you will see this';
    //}, 5000);

    //setTimeout(() => {
    //  console.log('second change');
    //  this.bookable3.title = "you won't see this!";
    //}, 8000);
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
