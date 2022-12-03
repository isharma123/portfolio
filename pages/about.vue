<template>
  <v-col class="my-2 mx-2">
    <h2 class="heading mb-3">
        About Me
    </h2>
    <v-row>
        <v-col cols="12" lg="6">
            <div>
                <v-img
                lazy-src="./me.jpeg"
                max-height="600"
                max-width="650"
                src="./me.jpeg"
                class="mx-auto"
                contain
                ></v-img>
            </div>
        </v-col>
        <v-col cols="12" lg="6">
            <div class="myself">
                I was always inspired to become an event planner. Ever since I started 
                studying Hospitality Management my instrest towards it became more keen. 
                After practical internships i was very confident about deciding my career in event planning. 
                I have oraganized lots of events in my former university. 
                I was president of MUN (Model United Nations) in my former university and most of my position
                 work included organizing to managing MUN events. I have also done internship for six months
                  in Leela Palace and Resort. From all those experiences my interest towards learning and starting
                   my career in hospitality and event management became deeper.
            </div>
        </v-col>
    </v-row>
    <v-row>
        <v-col cols="12" lg="6">
            <div>
                <v-img
                lazy-src="./me.jpeg"
                max-height="400"
                max-width="550"
                src="./prema.jpeg"
                class="mx-auto"
                contain
                ></v-img>
            </div>
        </v-col>
        <v-col cols="12" lg="6">
            <div class="myself">
                <div class="designation"><b><u>My Advisor</u></b></div>
                <b>Prema Monteiro, MS, EdS</b>
                <br>
                Professor of Culinary Arts Mgmt. / Hospitality and Events Mgmt. <br>
                Department of Visual Arts and Design <br>
                University of North Alabama <br>
                Box 5006 <br>
                Florence, AL 35632   <br>
                Office: East Campus, Room 302 <br>
                            1640 Tune Ave.  <br>
                            Florence, AL 35632 <br>
                Phone: 256-765-5227 <br>
                Email: pmonteiro@una.edu <br>
            </div>
        </v-col>
    </v-row>
  </v-col>
</template>

<script>
export default {
    name: 'about-me'
}
</script>

<style>
.myself{
    font-size: 1.3vw;
    margin: 0 auto;
    font-weight: 400;
    font-family: 'Libre Baskerville', serif;
}
</style>