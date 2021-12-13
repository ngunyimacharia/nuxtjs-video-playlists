<template>
    <video
        id="tag-source-player"
        controls
        autoplay
        class="cld-video-player cld-video-player-skin-dark w-1/2 mx-auto h-96"
    >
    </video>
</template>

<script>
export default {
    data(){
        return {
            cld: null,
            player:null,
        }
    },
    mounted(){
        this.cld = cloudinary.Cloudinary.new({ cloud_name: process.env.NUXT_ENV_CLOUDINARY_CLOUD_NAME, secure: true});

        this.player = this.cld.videoPlayer("tag-source-player");

        this.player.playlistByTag(
            "nvp-animals", 
            { autoAdvance: true, repeat: true, presentUpcoming: 8 }
        );
    }
}
</script>