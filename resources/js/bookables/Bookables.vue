<template>
  <div>
    Row is : {{ rows }}
    <div v-if="loading">
      <p>Loading...</p>
    </div>
    <div v-else>
      <div class="row mb-3" v-for="r in rows" :key="'row' + r">
        <div
          class="col"
          v-for="(b, i) in bookablesInRow(r)"
          :key="'row' + r + 'col' + i"
        >
          <BookableListItem
            :title="b.title"
            :content="b.content"
            :price="1500"
          />
        </div>
        <div
          class="col"
          v-for="p in placeholdersInRow(r)"
          :key="'placeholder' + r + p"
        ></div>
      </div>
    </div>
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
      bookables: null,
      loading: true,
      columns: 3,
    };
  },
  computed: {
    rows() {
      return !this.bookables
        ? 0
        : Math.ceil(this.bookables.length / this.columns);
    },
  },
  methods: {
    bookablesInRow(row) {
      return this.bookables.slice((row - 1) * this.columns, row * this.columns);
    },
    placeholdersInRow(row) {
      return this.columns - this.bookablesInRow(row).length;
    },
  },
  created() {
    this.loading = true;
    setTimeout(() => {
      this.bookables = [
        {
          title: 'Cheap Villa 1',
          content: 'a very cheap villa 1',
        },
        {
          title: 'Cheap Villa 2',
          content: 'a very cheap villa 2',
        },
        {
          title: 'Cheap Villa 3',
          content: 'a very cheap villa 3',
        },
        {
          title: 'Cheap Villa 4',
          content: 'a very cheap villa 4',
        },
        {
          title: 'Cheap Villa 5',
          content: 'a very cheap villa 5',
        },
        {
          title: 'Cheap Villa 6',
          content: 'a very cheap villa 6',
        },
        {
          title: 'Cheap Villa 7',
          content: 'a very cheap villa 7',
        },
      ];
      this.loading = false;
    }, 2000);
  },
};
</script>
