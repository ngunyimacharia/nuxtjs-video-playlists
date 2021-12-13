<template>
    <video
        id="fixed-source-player"
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
            sources:[
                "nuxtjs-video-playlist/production_ID_3987730.mp4",
                "nuxtjs-video-playlist/pexels-zlatin-georgiev-7173031.mp4",
                "nuxtjs-video-playlist/pexels-taryn-elliott-5220279.mp4",
                "nuxtjs-video-playlist/pexels-taryn-elliott-9116112.mp4",
                "nuxtjs-video-playlist/Pexels_Videos_1526909.mp4",
            ]
        }
    },
    mounted(){
        this.cld = cloudinary.Cloudinary.new({ cloud_name: process.env.NUXT_ENV_CLOUDINARY_CLOUD_NAME, secure: true});

        this.player = this.cld.videoPlayer(
            "fixed-source-player",
             {
                playlistWidget: {
                    direction:'vertical',
                    total:5
                }
             }
        );

        this.player.playlist(
            this.sources, 
            { autoAdvance: true, repeat: true, presentUpcoming: 8 }
        );
    }
}
</script>