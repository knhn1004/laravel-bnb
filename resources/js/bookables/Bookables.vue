<template>
  <div>
    <BookableListItem
      title="Cheap Villa"
      content="A very cheap villa"
      :price="1500"
    />
    <BookableListItem
      title="Cheap Villa2"
      content="A very cheap villa2"
      :price="1000"
    />
    <BookableListItem
      title="Cheap Villa3"
      content="A very cheap villa3"
      :price="500"
    />
  </div>
</template>

<script>
import BookableListItem from './BookableListItem';

export default {
  components: {
    BookableListItem,
  },
};
</script>
