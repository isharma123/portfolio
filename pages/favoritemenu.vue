<template>
  <v-container>
    <div class="heading">
        My Favorite Menu
    </div>
    <v-row>
      <v-col cols="6"  v-for="(item,i) in items" :key="i">
        <v-card
            :color="item.color"
            dark
          >
            <div class="d-flex flex-no-wrap justify-space-between">
              <div>
                <v-card-title
                  class="text-h5"
                  v-text="item.title"
                ></v-card-title>

                <v-card-subtitle v-text="item.artist"></v-card-subtitle>

                <v-card-actions>
                  <div class="text-center">
                      <v-dialog
                        v-model="item.d"
                        width="500"
                      >
                        <template v-slot:activator="{ on, attrs }">
                          <v-btn
                            color="red lighten-2"
                            dark
                            v-bind="attrs"
                            v-on="on"
                            text
                          >
                            View Receipe
                          </v-btn>
                        </template>

                        <v-card>
                          <v-card-title class="text-h5 grey lighten-2">
                            {{item.title}}
                          </v-card-title>

                          <v-card-text>
                            <ul>
                              <li v-for="(l,key) in item.receipe" :key="key">{{l}}</li>
                            </ul>
                          </v-card-text>

                          <v-divider></v-divider>

                          <v-card-actions>
                            <v-spacer></v-spacer>
                            <v-btn
                              color="primary"
                              text
                              @click="item.d = false"
                            >
                              Close
                            </v-btn>
                          </v-card-actions>
                        </v-card>
                      </v-dialog>
                    </div>
                </v-card-actions>
              </div>

              <v-avatar
                class="ma-3"
                size="125"
                tile
              >
                <v-img :src="item.src"></v-img>
              </v-avatar>
            </div>
          </v-card>
    </v-col>
    <v-col cols="12">
      <div class="expCol">
        <div class="exp">
          My most successful menu was when I cooked for my family at one Family Function. I cooked Indian cuisine for my family back in 2021 and everyone loved that.
        </div>
        <div class="exp">
          Butter chicken originated from Northern India in 1948. Created by Kundan Lal Gujral, you may notice that Butter Chicken (known as murgh makhani — chicken with butter), is similar to British tikka masala.

  Prepared in a buttery gravy with the addition of cream gives the curry sauce a silky smooth rich texture. Most restaurants are known to add in copious amounts of butter, which as a result can leave you feeling bloated or ill from the slick of grease.

  However, we found while recipe testing that we prefer to start the sauce off in Ghee (clarified butter, or you can use a combination of half regular butter and half oil).

  Adding cream at the end of cooking provides enough of that richness you look for in an authentic butter chicken. Our less oily version leaves you feeling good and satisfied.
        </div>
      </div>
    </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'menu',   
    data: () => ({
      dialog: false,
      dialog1: false,
      items: [
        {
          color: '#1F7087',
          src: 'https://c8.alamy.com/comp/KJJHKE/mutton-masala-or-masala-gosht-or-indian-lamb-rogan-josh-with-some-KJJHKE.jpg',
          title: 'Mutton Rogan Josh',
          d: false,
          artist: 'I cooked Mutton Rogan Josh with white rice and Naan. Naan is Indian style flatbread which is cooked in the Tandoor. Mutton Rogan Josh consist pf Pieces of lamb braised with gravy flavoured with garlic, ginger and aromatic spices. After braising , the dish may be finished using the slow cooking technique.',
          adddesc: 'My most successful menu was when I cooked for my family at one Family Function. I cooked Indian cuisine for my family back in 2021 and everyone loved that.'
          ,receipe: ['Marinate mutton with yogurt, half of the garlic, half of the ginger and salt.', 
                    'Cover and refrigerate for six to eight hours.', 
                    'Heat ghee in a non stick pan.',
                    'Add cinnamon, cloves, black cardamom, green cardamoms. Sauté for two minutes.',
                    'Add onions, remaining garlic and ginger and sauté till onions are golden brown.',
                    'Add coriander powder, cumin powder, fennel powder, red chilli powder.', 
                    'Mix well and sauté for five minutes.', 
                    'Add marinated mutton. Sauté for eight to ten minutes.',
                  'Add chicken stock, cover and simmer for fifty to sixty minutes.',
                  'Cook uncovered for ten to fifteen minutes more.',
                  'Sprinkle garam masala powder and mix well.',
                  'Serve hot garnished with mint and coriander leaves.']
        },
        {
          color: '#78e08f',
          src: 'https://images.squarespace-cdn.com/content/v1/594164dc2e69cffcdb5206e1/1609951624959-8R9CV4G5XMC8I9HL35FQ/ke17ZwdGBToddI8pDm48kBRDepl_S0Ckh03lhQnAKgR7gQa3H78H3Y0txjaiv_0fDoOvxcdMmMKkDsyUqMSsMWxHk725yiiHCCLfrh8O1z5QPOohDIaIeljMHgDF5CVlOqpeNLcJ80NK65_fV7S1UQcXx0vq6RDfSrirApoTEGSRUgS85Gvixf9-m4YnswWU1_uf9fLFr4UlaesQEh5GoQ/Homestyle+Butter+Chicken+1.jpg',
          title: 'Butter Chicken',
          d: false,
          artist: 'Butter chicken, traditionally known as murgh makhani, is an Indian dish originating in New Delhi. It is a type of curry made from chicken with a spiced tomato and butter sauce. Its sauce is known for its rich texture. It is similar to chicken tikka masala, which uses a tomato paste.',
          adddesc: 'My most successful menu was when I cooked for my family at one Family Function. I cooked Indian cuisine for my family back in 2021 and everyone loved that.'
          ,receipe: ['Ingredients', '1 tablespoon oil'
,'1 tablespoon butter'
,'1 medium onion diced'
,'1 teaspoon fresh ginger finely minced or grated (or use paste)'
,'2-3 cloves garlic finely minced or crushed'
,'1 ½ pounds about 2-3 boneless, skinless chicken breasts, cut into ¾-inch chunks'
,'4 tablespoons tomato paste or 8 oz can of tomato sauce'
,'1 tablespoon garam masala'
,'1 teaspoon  or paprika, adjust to taste'
,'1 teaspoon Fenugreek I use powder, but seeds or mustard seeds can be used too, optional'
,'1 teaspoon '
,'1 tsp salt',

'1/4 tsp black pepper',
'1 cup heavy cream sub for half & half or yogurt for low fat',
'Hot cooked rice and naan for serving', 
'Recipe',
'Heat a large skillet or medium saucepan over medium-high heat. Add the oil, butter, and onions and cook onions down until lightly golden, about 3-4 minutes. Add ginger and garlic and let cook for 30 seconds, stirring so it doesn’t burn.',"2. Add the chicken, tomato paste, and spices. Cook for 5-6 minutes or until everything is cooked through.","3. Add the heavy cream and simmer for 8-10 minutes stirring occasionally. Serve over Basmati rice or with naan."],
        },
      ],
    }),
  }
</script>

<style scoped>
html{
}
.expCol{
  font-family: 'Libre Baskerville', serif;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
}
.exp{
  font-size: 1.5em;
  margin: 20px auto;
}
</style>