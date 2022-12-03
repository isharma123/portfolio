<template>
  <v-col class="px-0">
    <div class="banner">
      <img class="image" src="https://source.unsplash.com/random/900×700/?hotel,culinary,italian food,icecream,english food" alt="photo">
    </div>
    <div class="mytitle">
      Student of <br> <b>Event & Hospitality Management</b>
    </div>
    <div class="message d-flex d-flex-column">
      <v-card
        class=" ml-6 mr-auto"
        color="#26c6da"
        dark
        flat
        max-width="400"
      >
        <v-card-text class="text-h5 font-weight-bold">
          "My culinary education is helping me grow professinally by allowing me to practice and study the skills needed to become a Hoteliar. I'm learning self dicipline, patience, professionalism."
        </v-card-text>

        <v-card-actions>
          <v-list-item class="grow">
            <v-list-item-avatar color="grey darken-3">
              <v-img
                class="elevation-6"
                alt=""
                src="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
              ></v-img>
            </v-list-item-avatar>

            <v-list-item-content>
              <v-list-item-title>Ishant</v-list-item-title>
            </v-list-item-content>

            <v-row
              align="center"
              justify="end"
            >
              <v-icon class="mr-1">
                mdi-heart
              </v-icon>
            </v-row>
          </v-list-item>
        </v-card-actions>
      </v-card>
      <img class="gussiphoto1" src="https://www.theeventor.in/wp-content/uploads/2020/04/Avani_-Hua-Hin-Indian-Wedding-The-Eventor-9.3-1024x651.jpg" alt="photo">
      <img class="gussiphoto2" src="https://www.hoteleventi.com/images/1700-960/eventi-veranda-ea0518cc.jpg" alt="photo">
      <img class="gussiphoto3" src="https://images.squarespace-cdn.com/content/517c9ee6e4b0f470ac8e5ab8/1462188289703-2VT071YC0NIBWFBOBDLO/?format=1000w&content-type=image%2Fjpeg" alt="photo">
    </div>
    <v-parallax class="my-6" src="https://boomersdaily.files.wordpress.com/2020/01/ambiente-sedona-landscape-hotel-facebook.jpg"></v-parallax>
    
  </v-col>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
<style scoped>
.banner{
  height: 300px;
}
.image{
  height: 300px;
  width: 100%;
  object-fit: cover;
}
.mytitle{
  text-align: center;
  margin: 50px auto;
  font-size: 1.8vw;
    font-family: 'Libre Baskerville', serif;
}
.message{
  position: relative;
}
.gussiphoto1{
  width: 350px;
  height: 180px;
  position: absolute;
  top: 80px;
  left: 400px;
}
.gussiphoto2{
  width: 350px;
  height: 180px;
  position: absolute;
  top: 150px;
  right: -50px;
  /* left: 400px; */
}
.gussiphoto3{
  width: 350px;
  height: 180px;
  position: absolute;
  top: 0px;
  left: 740px;
}
</style>
