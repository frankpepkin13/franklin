<template>
  <div class="container mx-auto px-4 lg:px-0 py-8">
    <h1 class="text-4xl font-bold mb-8 text-blue-600 text-center lg:text-left">Crazy Dictionary</h1>
    <div class="w-full lg:w-3/4 xl:w-1/2 mx-auto lg:mx-0">
      <input type="text" v-model="searchTerm" placeholder="Search for a word..."
        class="w-full px-4 py-2 border border-gray-300 rounded-md mb-4 focus:outline-none focus:ring focus:border-blue-400 text-lg"
        @keyup.enter="searchDictionary" />
    </div>
    <div v-if="selectedWord" class="w-full lg:w-3/4 xl:w-1/2 mx-auto lg:mx-0">
      <div class="bg-white shadow-md rounded-md p-6 text-left text-gray-800">
        <h2 class="text-2xl font-semibold mb-4 text-blue-600">{{ selectedWord.word }}</h2>
        <p class="text-lg">{{ selectedWord.definition }}</p>
      </div>
    </div>
    <p v-if="errorMessage" class="text-red-500 mt-2 text-left">{{ errorMessage }}</p>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      searchTerm: '',
      selectedWord: null,
      errorMessage: ''
    };
  },
  methods: {
    async searchDictionary() {
      try {
        const response = await axios.get(`https://api.urbandictionary.com/v0/define?term=${this.searchTerm}`);
        if (response.data.list.length > 0) {
          // Get the first definition from the response
          this.selectedWord = {
            word: response.data.list[0].word,
            definition: response.data.list[0].definition
          };
          
          this.errorMessage = ''; // Clear any previous error messages
        } else {
          this.selectedWord = null;
          this.errorMessage = 'Word not found';
        }
      } catch (error) {
        this.selectedWord = null;
        this.errorMessage = 'Failed to fetch data';
      }
    }
  }
};
</script>

<style scoped>
/* You can add global styles here if needed */
/* Example of adding some spacing and font styles */
h1 {
  margin-bottom: 1.5rem;
  font-family: 'Arial', sans-serif;
}
</style>
