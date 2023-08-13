<script setup>
import { onMounted, ref } from 'vue'
import movies from './movies.json'

import Magnify from 'vue-material-design-icons/Magnify.vue'
import HomeOutline from 'vue-material-design-icons/HomeOutline.vue'
import TrendingUp from 'vue-material-design-icons/TrendingUp.vue'
import Television from 'vue-material-design-icons/Television.vue'
import MovieOutline from 'vue-material-design-icons/MovieOutline.vue'
import Plus from 'vue-material-design-icons/Plus.vue'
import ChevronLeft from 'vue-material-design-icons/ChevronLeft.vue'

import { useMovieStore } from './stores/movie'
import { storeToRefs } from 'pinia'
const useMovie = useMovieStore()
const { movie, showFullVideo } = storeToRefs(useMovie)

let video = ref(null)

onMounted(() => {
  setTimeout(() => (movie.value = movies[0][0]), 100)
})
</script>

<template>
  <h1 class="text-3xl font-bold underline">Hello world!</h1>
</template>
