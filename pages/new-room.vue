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
            ルーム情報の入力
          </v-stepper-step>

          <v-divider></v-divider>

          <v-stepper-step
            :complete="e1 > 2"
            step="2"
          >
            共有範囲の設定
          </v-stepper-step>

          <v-divider></v-divider>

          <v-stepper-step
            :complete="e1 > 2"
            step="3"
          >
            友達を招待
          </v-stepper-step>
        </v-stepper-header>

        <v-stepper-items>
          <v-stepper-content step="1">
            <p>新規作成するルームの情報を入力してください</p>
            <v-row>
              <v-col
                cols="12"
                d-flex justify-center
              >
                <v-text-field
                  v-model="roomname"
                  :rules="nameRules"
                  :counter="64"
                  label="ルーム名"
                  required
                ></v-text-field>
              </v-col>

              <v-col
                cols="12"
                d-flex justify-center
              >
                <v-textarea
                  v-model="lastname"
                  :rules="nameRules"
                  :counter="300"
                  label="ルームの説明"
                  required
                ></v-textarea>
              </v-col>
              <v-col
                cols="12"
                d-flex justify-center
              >
                <v-select
                  :items="['なし','Slack','Discord','LINE']"
                  label="通知先のアプリ(任意)"
                ></v-select>

                <v-text-field
                    v-model="notificationurl"
                    :rules="nameRules"
                    label="通知先のURL(任意)"
                  ></v-text-field>
              </v-col>
              <v-col
                cols="12"
                d-flex justify-center
              >
                ルームカラー
                <v-color-picker
                  v-model="color"
                ></v-color-picker>
              </v-col>
            </v-row>

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

            〇〇ルームに対する、カレンダー共有の設定をお願いします

            <div class="my-5">
              <v-list>
                <ListItemCalenderPermission />
                <ListItemCalenderPermission />
                <ListItemCalenderPermission />
              </v-list>
            </div>

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

            作成が完了しました。次のリンクを共有して参加者を招待してください。

            <v-col cols="12">
              <v-text-field
                v-model="message"
                append-icon="mdi-clipboard-outline"
                filled
                marker
                label="共有用URL"
                type="text"
              ></v-text-field>
            </v-col>

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
  name: 'NewRoomPage',
  layout: 'app',
  data () {
      return {
        e1: 1,
      }
  }
}
</script>
