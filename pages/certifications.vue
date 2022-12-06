<template>
    <v-col>
        <div class="heading my-3">
            Certifications
        </div>
        <v-row class="cardCert" v-for="(item,i) in data" :key="i">
        <v-col cols="12" lg="6">
            <div>
                <v-img
                class="imageCert"
                :lazy-src="item.link"
                max-height="450"
                max-width="500"
                :src="item.link"
                ></v-img>
            </div>
        </v-col>
        <v-col  class="myself" cols="12" lg="6">
            <div class="image">
                <v-img :lazy-src="item.img" :src="item.img"></v-img>
            </div>
            <div>
                {{item.text}}
            </div>
        </v-col>
    </v-row>
    </v-col>
  </template>
<script>
export default {
    name: 'certifications',
    data(){
        return {
            data: [
                {
                    link:'./leela.jpeg',
                    text: 'Back In my country India, I did my Internship In 5 star resort, THE LEELA PALACE JAIPUR. That was one of the best experince of my life. The Leela Palace Jaipur is located in Jamwa Ramgarh. This hotel is has an amazing mix of legacy and modern extravagance.',
                    img: 'https://ihaviationandtravel.files.wordpress.com/2021/02/img_5833.jpg?w=2048'
                },
                {
                    link:'./certficate.jpeg',
                    text: null
                },
                {
                    link:'./english.jpeg',
                    text: null
                },
                {
                    link:'./Screenshot 2022-12-05 182530.png',
                    text: null
                },
                {
                    link:'./Screenshot 2022-12-05 182559.png',
                    text: null
                },
            ]
        }
    }
}
</script>

<style>
.imageCert{
    margin: auto;
    border-radius: 10px;
    object-fit: contain;
}
.v-image .v-image__image--cover{
    background-size: contain !important;
}
.cardCert{
    margin: 10px auto;
    font-family: 'Libre Baskerville', serif;
    font-size: 1.2em;
}
.myself{
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-self: center;
}
</style>
