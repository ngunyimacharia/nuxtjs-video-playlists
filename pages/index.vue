<template>
  <div>
    <h1 class="text-center text-2xl leading-8 font-extrabold tracking-tight text-gray-700 m-12 ">
      Fixed source playlist with widget
    </h1>
    
    <fixed-source-playlist class="m-24"/>
    
    <h1 class="text-center text-2xl leading-8 font-extrabold tracking-tight text-gray-700 m-12 ">
      Tag specific playlist without widget
    </h1>

    <tag-specific-playlist class="m-24"/>
  </div>
</template>

<script>
import FixedSourcePlaylist from '../components/FixedSourcePlaylist.vue'
import TagSpecificPlaylist from '../components/TagSpecificPlaylist.vue'

export default {
  name: 'IndexPage',
  components: { 
    FixedSourcePlaylist, 
    TagSpecificPlaylist
  },
}
</script>
