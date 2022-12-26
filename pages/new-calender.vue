<template>
  <v-row justify="center" align="center">
    <v-col cols="12" xs5>
      カレンダーの追加
    </v-col>
    <v-col cols="12">
      <v-stepper v-model="e1">
        <v-stepper-header>
          <v-stepper-step
            :complete="e1 > 1"
            step="1"
          >
            取得方法の入力
          </v-stepper-step>

          <v-divider></v-divider>

          <v-stepper-step
            :complete="e1 > 2"
            step="2"
          >
            カレンダー連携
          </v-stepper-step>

          <v-divider></v-divider>

          <v-stepper-step
            :complete="e1 > 2"
            step="3"
          >
            取得内容の確認
          </v-stepper-step>
        </v-stepper-header>

        <v-stepper-items>
          <v-stepper-content step="1">
            <v-card
              class="mb-12"
              color="grey lighten-1"
              height="200px"
            ></v-card>

            <v-btn
              color="primary"
              @click="e1 = 2"
            >
              次へ
            </v-btn>

            <v-btn text>
              キャンセル
            </v-btn>
          </v-stepper-content>

          <v-stepper-content step="2">
            <v-card
              class="mb-12"
              color="grey lighten-1"
              height="200px"
            ></v-card>

            <v-btn
              color="primary"
              @click="e1 = 3"
            >
              次へ
            </v-btn>

            <v-btn text>
              キャンセル
            </v-btn>
          </v-stepper-content>

          <v-stepper-content step="3">
            <v-card
              class="mb-12"
              color="grey lighten-1"
              height="200px"
            ></v-card>

            <v-btn
              color="primary"
              to="/room"
            >
              完了
            </v-btn>
          </v-stepper-content>
        </v-stepper-items>
      </v-stepper>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'NewRoomPage',
  layout: 'app',
  data () {
      return {
        e1: 1,
      }
  }
}
</script>
