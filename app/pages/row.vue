<template>
  <div>
    <v-row>
      <v-col cols="12" md="3">
        <v-card
          height="100"
          elevation="0"
          color="#EEEEEE"
          class="card-margin-blue"
        >
          <v-card-text>
            <v-row>
              <v-col cols="4">
                <v-progress-circular
                  :model-value="28"
                  :rotate="360"
                  :size="60"
                  :width="8"
                  color="blue"
                >
                  28%
                </v-progress-circular>
              </v-col>
              <v-col cols="8">
                <v-row dense>
                  <v-col cols="12" class="text-right font-weight-bold">
                    Student
                  </v-col>
                  <v-col cols="12" class="text-right text-h4 font-weight-bold">
                    120
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="12" md="3">
        <v-card
          height="100"
          elevation="0"
          color="#EEEEEE"
          class="card-margin-orange"
        >
          <v-card-text>
            <v-row>
              <v-col cols="4">
                <v-progress-circular
                  :model-value="58"
                  :rotate="360"
                  :size="60"
                  :width="8"
                  color="orange"
                >
                  58%
                </v-progress-circular>
              </v-col>
              <v-col cols="8">
                <v-row dense>
                  <v-col cols="12" class="text-right font-weight-bold">
                    Account
                  </v-col>
                  <v-col cols="12" class="text-right text-h4 font-weight-bold">
                    234
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="12" md="3">
        <v-card
          height="100"
          elevation="0"
          color="#EEEEEE"
          class="card-margin-red"
        >
          <v-card-text>
            <v-row>
              <v-col cols="4">
                <v-progress-circular
                  :model-value="71"
                  :rotate="360"
                  :size="60"
                  :width="8"
                  color="red"
                >
                  71%
                </v-progress-circular>
              </v-col>
              <v-col cols="8">
                <v-row dense>
                  <v-col cols="12" class="text-right font-weight-bold">
                    Expenses
                  </v-col>
                  <v-col cols="12" class="text-right text-h4 font-weight-bold">
                    62
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="12" md="3">
        <v-card
          height="100"
          elevation="0"
          color="#EEEEEE"
          class="card-margin-green"
        >
          <v-card-text>
            <v-row>
              <v-col cols="4">
                <v-progress-circular
                  :model-value="81"
                  :rotate="360"
                  :size="60"
                  :width="8"
                  color="green"
                >
                  81%
                </v-progress-circular>
              </v-col>
              <v-col cols="8">
                <v-row dense>
                  <v-col cols="12" class="text-right font-weight-bold">
                    New employees
                  </v-col>
                  <v-col cols="12" class="text-right text-h4 font-weight-bold">
                    34
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="8">
        <v-card>
          <v-card-text>
            <v-data-table :headers="headers" :items="plants"></v-data-table>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="4">
        <v-row>
          <v-col cols="12">
            <v-card color="#385F73">
              <v-card-title class="text-h5"> Unlimited music now </v-card-title>

              <v-card-subtitle>
                Listen to your favorite artists and albums whenever and
                wherever, online and offline.
              </v-card-subtitle>

              <v-card-actions>
                <v-btn text="Listen Now" variant="text"></v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
          <v-col cols="12">
            <v-card color="#1F7087">
              <div class="d-flex flex-no-wrap justify-space-between">
                <div>
                  <v-card-title class="text-h5"> Supermodel </v-card-title>

                  <v-card-subtitle>Foster the People</v-card-subtitle>

                  <v-card-actions>
                    <v-btn
                      class="ms-2"
                      size="small"
                      text="START RADIO"
                      variant="outlined"
                    ></v-btn>
                  </v-card-actions>
                </div>

                <v-avatar class="ma-3" rounded="0" size="125">
                  <v-img
                    src="https://cdn.vuetifyjs.com/images/cards/foster.jpg"
                  ></v-img>
                </v-avatar>
              </div>
            </v-card>
          </v-col>
          <v-col cols="12">
            <v-card color="#952175">
              <div class="d-flex flex-no-wrap justify-space-between">
                <div>
                  <v-card-title class="text-h5"> Halcyon Days </v-card-title>

                  <v-card-subtitle>Ellie Goulding</v-card-subtitle>

                  <v-card-actions>
                    <v-btn class="ms-2" icon="mdi-play" variant="text"></v-btn>
                  </v-card-actions>
                </div>

                <v-avatar class="ma-3" rounded="0" size="125">
                  <v-img
                    src="https://cdn.vuetifyjs.com/images/cards/halcyon.png"
                  ></v-img>
                </v-avatar>
              </div>
            </v-card>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<script setup>
const headers = [
  { title: "Plant", align: "start", sortable: false, key: "name" },
  { title: "Light", align: "end", key: "light" },
  { title: "Height", align: "end", key: "height" },
  { title: "Pet Friendly", align: "end", key: "petFriendly" },
  { title: "Price ($)", align: "end", key: "price" },
];

const plants = [
  {
    name: "Fern",
    light: "Low",
    height: "20cm",
    petFriendly: "Yes",
    price: 20,
  },
  {
    name: "Snake Plant",
    light: "Low",
    height: "50cm",
    petFriendly: "No",
    price: 35,
  },
  {
    name: "Monstera",
    light: "Medium",
    height: "60cm",
    petFriendly: "No",
    price: 50,
  },
  {
    name: "Pothos",
    light: "Low to medium",
    height: "40cm",
    petFriendly: "Yes",
    price: 25,
  },
  {
    name: "ZZ Plant",
    light: "Low to medium",
    height: "90cm",
    petFriendly: "Yes",
    price: 30,
  },
  {
    name: "Spider Plant",
    light: "Bright, indirect",
    height: "30cm",
    petFriendly: "Yes",
    price: 15,
  },
  {
    name: "Air Plant",
    light: "Bright, indirect",
    height: "15cm",
    petFriendly: "Yes",
    price: 10,
  },
  {
    name: "Peperomia",
    light: "Bright, indirect",
    height: "25cm",
    petFriendly: "Yes",
    price: 20,
  },
  {
    name: "Aloe Vera",
    light: "Bright, direct",
    height: "30cm",
    petFriendly: "Yes",
    price: 15,
  },
  {
    name: "Jade Plant",
    light: "Bright, direct",
    height: "40cm",
    petFriendly: "Yes",
    price: 25,
  },
];
</script>

<style scoped>
.card-margin-blue {
  border-bottom: 7px solid #2196f3;
}
.card-margin-orange {
  border-bottom: 7px solid #ff9800;
}
.card-margin-red {
  border-bottom: 7px solid #f44336;
}
.card-margin-green {
  border-bottom: 7px solid #4caf50;
}
</style>