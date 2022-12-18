<template>
  <div>
    <h1>{{ title }}</h1>
    <ul>
      <Book-Item v-for="book in books" :book="book"></Book-Item>
    </ul>
  </div>
</template>

<script>
  import BookItem from './BookItem.vue';
  export default {
    name: "Book-List",    
    data() {
      return {
        title: "All Books",
        books: [
            {title: 'Self-Reliance', author: 'Ralph Waldo Emerson'},
            {title: 'American Gods', author: 'Neil Gaiman'},
            {title: 'Amusing Ourselves to Death', author: 'Neil Postman'},
        ]
      }
    },
    components: {
      BookItem,
    } 
  };
</script>

<style>
  h1, h2 {
    font-weight: normal;
  }
  ul {
    list-style-type: none;
    padding: 0;    
  }  
</style>