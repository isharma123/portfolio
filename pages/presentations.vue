<template>
  <v-col class="my-2 mx-4">
    <div class="heading my-3">
            Video Presentation
    </div>
    <div class="mx-auto">
      <iframe width="560" height="315" src="https://www.youtube.com/embed/o94qJGT3Vqg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
    </div>
    <p class="description">
        As my major is Hospitality and Events Management, 
        Fron office department is one of the major section of my major. 
        In the following vedio I have presented the check- In procedure of the hotel as an front office assistant. 
        Click here to watch the video.
    </p>
  </v-col>
</template>

<script>
export default {
    name: 'presentations',
    data() {
    return {
    };
  }
}
</script>

<style scoped>
.video{
  text-align: center;
}
.description{
  font-size: 1.8vw;
  font-weight: lighter;
}
</style>
