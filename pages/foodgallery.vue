<template>
  <v-col class="my-3 mx-4">
    <h2 class="heading">Food Photos</h2>
    <v-row>
        <v-col sm="12" md="4" lg="3" v-for="(item,i) in food" :key="i">
            <v-card
                :loading="loading"
                class="mx-auto my-3"
                max-width="374"
            >
                <template slot="progress">
                <v-progress-linear
                    color="deep-purple"
                    height="10"
                    indeterminate
                ></v-progress-linear>
                </template>
    
                <v-img
                height="250"
                :src="item.link == null ? 'https://cdn.vuetifyjs.com/images/cards/cooking.png' : item.link"
                ></v-img>
    
                <v-card-title>{{item.name}}</v-card-title>
    
                <v-card-text>    
                <div>{{item.desc}}</div>
                </v-card-text>
            </v-card>
        </v-col>
    </v-row>
  </v-col>
</template>

<script>
export default {
    name: 'food-gallery',
    data(){
        return{
            food:[
                {
                    name: "Cheese Board",
                    link: './food/food1.jpeg',
                    cusine: "Italian",
                    desc: 'The Cheese Board Collective in Berkeley, California, comprises two worker-owned and -operated businesses: a cheese shop/bakery commonly referred to as "The Cheese Board", and a pizzeria known as "Cheese Board Pizza"'
                },
                {
                    name: "Grape & Cheese Canape",
                    link: './food/food2.jpeg',
                    cusine: "Italian",
                    desc: "Tangy blue cheese, crunchy walnuts, and juicy sweet grapes pair beautifully together in this blue cheese appetizer. Serve it as the perfect party food for holiday gatherings, weddings, baby showers, or any other special occasion that calls for something tasty. It's simple to prepare and the individual portions present well for serving."
                },
                {
                    name: "Papaya Salad",
                    link: './food/food3.jpeg',
                    cusine: "Italian",
                    desc: `The Cheese Board Collective in Berkeley, California, comprises two worker-owned and -operated businesses: a cheese shop/bakery commonly referred to as "The Cheese Board", and a pizzeria known as "Cheese Board Pizza"`
                },
                {
                    name: "Avocado Cheese Toast",
                    link: './food/food4.jpeg',
                    cusine: "Italian",
                    desc: `Make your avocado toast just a little creamier with the addition of melted cheese! So simple yet so delicious and perfect for breakfast or lunch! This recipe includes Colby Jack cheese but feel free to swap for your favorite. One of our favorite combinations is avocado toast with goat cheese.`
                },
                {
                    name: "Healty Marinated Asparagus Salad",
                    link: './food/food5.jpeg',
                    cusine: "Italian",
                    desc: 'Salads that are filled with more vegetables and fruit in them than lettuce make my day! For more flavored salads try this Antipasto Salad Recipe, Apple Bacon Brussels Sprouts Salad or Avocado, Tomato and Cucumber Arugula Salad.'
                },
            ]
        }
    }
}
</script>

<style>

</style>