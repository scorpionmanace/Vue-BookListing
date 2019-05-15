<template>
  <form class="" actions="#" method="post" @submit.prevent="bookSubmit(bookTitle, bookAuthor)">
    <input v-model="bookTitle" type="text" name="title" value="" placeholdere="Book Title"/>
    <input v-model="bookAuthor" type="text" name="title" value="" placeholdere="Book Authot"/>
    <button type="submit" name="button">Add Book</button>
  </form>
</template>

<script>
export default {
  name: 'BookForm',
  props: ['books'],
  data() {
    return {
      bookTitle: '',
      bookAuthor: ''
    }
  },
  methods: {
    bookSubmit(bookTitle, bookAuthor) {
      this.$emit('addBook',bookTitle, bookAuthor);
    }
  }
}
</script>

<style>

</style>
