<template>
  <div>
    <v-row>
      <v-col cols="12" md="3">
        <v-card
          height="120"
          elevation="0"
          color="#EEEEEE"
          class="card-margin-blue"
        >
          <v-card-text>
            <v-row align="center">
              <v-col cols="4">
                <v-progress-circular
                  :model-value="28"
                  :rotate="360"
                  :size="80"
                  :width="8"
                  color="blue"
                >
                  28%
                </v-progress-circular>
              </v-col>
              <v-col cols="8">
                <v-row no-gutters>
                  <v-col
                    cols="12"
                    class="text-right text-uppercase font-weight-bold"
                  >
                    Student
                  </v-col>
                  <v-col cols="12" class="text-right text-h3 font-weight-bold">
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
          height="120"
          elevation="0"
          color="#EEEEEE"
          class="card-margin-orange"
        >
          <v-card-text>
            <v-row align="center">
              <v-col cols="4">
                <v-progress-circular
                  :model-value="58"
                  :rotate="360"
                  :size="80"
                  :width="8"
                  color="orange"
                >
                  58%
                </v-progress-circular>
              </v-col>
              <v-col cols="8">
                <v-row dense>
                  <v-col
                    cols="12"
                    class="text-right text-uppercase font-weight-bold"
                  >
                    Account
                  </v-col>
                  <v-col cols="12" class="text-right text-h3 font-weight-bold">
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
          height="120"
          elevation="0"
          color="#EEEEEE"
          class="card-margin-red"
        >
          <v-card-text>
            <v-row align="center">
              <v-col cols="4">
                <v-progress-circular
                  :model-value="71"
                  :rotate="360"
                  :size="80"
                  :width="8"
                  color="red"
                >
                  71%
                </v-progress-circular>
              </v-col>
              <v-col cols="8">
                <v-row dense>
                  <v-col
                    cols="12"
                    class="text-right text-uppercase font-weight-bold"
                  >
                    Expenses
                  </v-col>
                  <v-col cols="12" class="text-right text-h3 font-weight-bold">
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
          height="120"
          elevation="0"
          color="#EEEEEE"
          class="card-margin-green"
        >
          <v-card-text>
            <v-row align="center">
              <v-col cols="4">
                <v-progress-circular
                  :model-value="81"
                  :rotate="360"
                  :size="80"
                  :width="8"
                  color="green"
                >
                  81%
                </v-progress-circular>
              </v-col>
              <v-col cols="8">
                <v-row dense>
                  <v-col
                    cols="12"
                    class="text-right text-uppercase font-weight-bold"
                  >
                    New employees
                  </v-col>
                  <v-col cols="12" class="text-right text-h3 font-weight-bold">
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
        <v-card height="530" elevation="0" color="#EEEEEE"></v-card>
      </v-col>
      <v-col cols="4">
        <v-row>
          <v-col cols="12">
            <v-card height="160" elevation="0" color="#EEEEEE"></v-card>
          </v-col>
          <v-col cols="12">
            <v-card height="160" elevation="0" color="#EEEEEE"></v-card>
          </v-col>
          <v-col cols="12">
            <v-card height="160" elevation="0" color="#EEEEEE"></v-card>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
    <!-- Bottom fab button -->
    <v-fab
      :absolute="false"
      :app="true"
      color="primary"
      location="right bottom"
      size="large"
      icon
      @click="dialog = !dialog"
    >
      <v-icon>mdi-plus</v-icon>
    </v-fab>

    <!-- Dialog box -->
    <v-dialog v-model="dialog" width="500">
      <v-card>
        <v-toolbar>
          <v-toolbar-title>Create New Item</v-toolbar-title>
        </v-toolbar>
        <v-card-text>
          <v-form>
            <v-text-field
              label="Student no"
              variant="solo-filled"
              flat
            ></v-text-field>
            <v-text-field
              label="Name"
              variant="solo-filled"
              flat
            ></v-text-field>

            <v-text-field
              label="Course"
              variant="solo-filled"
              flat
            ></v-text-field>
          </v-form>
        </v-card-text>
        <v-card-actions>
          <v-btn color="primary" variant="flat" block>Create</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>

<script setup>
const dialog = ref(false);
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