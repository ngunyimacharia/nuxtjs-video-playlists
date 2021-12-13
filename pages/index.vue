<template>
  <div>
    <h1 class="text-center text-2xl leading-8 font-extrabold tracking-tight text-gray-700 m-12 ">Fixed source playlist</h1>
    <fixed-source-playlist class="m-24"/>
  </div>
</template>

<script>
import FixedSourcePlaylist from '../components/FixedSourcePlaylist.vue'
export default {
  components: { FixedSourcePlaylist },
  name: 'IndexPage'
}
</script>
