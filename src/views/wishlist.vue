<template>
    <div class="wishlist">
      <h1>📚 Wishlist Buku</h1>
      <div v-if="wishlist.length === 0">Belum ada buku di wishlist.</div>
      <ul>
        <li v-for="book in wishlist" :key="book.id">
          <img :src="book.imageUrl" alt="cover" style="width: 100px;" />
          <strong>{{ book.title }}</strong>
          <button @click="remove(book.id)">❌ Hapus</button>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
  name: 'Wishlist'
}
  
  </script>
  