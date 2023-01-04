<template>
  <v-row justify="center" align="center">
    <v-col cols="12" xs5>
      ルームの新規作成
    </v-col>
    <v-col cols="12">
      <v-stepper v-model="e1">
        <v-stepper-header>
          <v-stepper-step
            :complete="e1 > 1"
            step="1"
          >
            ルームの入力
          </v-stepper-step>

          <v-divider></v-divider>

          <v-stepper-step
            :complete="e1 > 2"
            step="2"
          >
            情報の確認
          </v-stepper-step>

          <v-divider></v-divider>

          <v-stepper-step
            :complete="e1 > 3"
            step="3"
          >
            権限設定
          </v-stepper-step>

          <v-divider></v-divider>

          <v-stepper-step
            :complete="e1 > 3"
            step="4"
          >
            承認待ち
          </v-stepper-step>

        </v-stepper-header>

        <v-stepper-items>
          <v-stepper-content step="1">

            ルームの管理者から提示されたルームIDを入力してください。
            <v-text-field
              label="ルームID"
            ></v-text-field>

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

            あなたは以下のルームに招待されています。参加しますか？

            <v-card
              class="my-8"
              outlined
            >
              <v-row>
                <v-col>
                  <div class="text-center my-5">
                    <v-avatar
                      color="yellow darken-3"
                      size="100"
                    >
                      <v-icon x-large dark>mdi-door-closed</v-icon>
                    </v-avatar>
                    <p class="my-7 mx-10 text-h5">あああルーム</p>
                    <p class="my-7 mx-12 text-subtitle-1">説明あああああああああああああああああああああああああああああああああああああああああああああああああああああ</p>
                  </div>
                </v-col>
              </v-row>          
            </v-card>

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
            〇〇ルームで共有するカレンダーの権限を設定してください。

            <div class="my-5">
              <v-list>
                <ListItemCalenderPermission />
                <ListItemCalenderPermission />
                <ListItemCalenderPermission />
              </v-list>
            </div>

            <v-btn
              color="primary"
              @click="e1 = 4"
            >
              次へ
            </v-btn>

            <v-btn text>
              キャンセル
            </v-btn>
          </v-stepper-content>

          <v-stepper-content step="4">
            <p>〇〇ルームへの参加申請が完了しました。申請がルームの管理者に許可されると、カレンダーにアクセスできるようになります。</p>

            <v-btn
              color="primary"
              to="/"
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
  name: 'JoinRoomPage',
  layout: 'app',
  data () {
      return {
        e1: 1,
      }
  }
}
</script>
