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
            連携カレンダーの選択
          </v-stepper-step>

          <v-divider></v-divider>

          <v-stepper-step
            :complete="e1 > 2"
            step="3"
          >
            権限設定
          </v-stepper-step>
        </v-stepper-header>

        <v-stepper-items>
          <v-stepper-content step="1">

            <p>追加したいカレンダーのあるサービスを選択してください。</p>

            <div class="text-center">
              <div class="my-5">
                <v-btn
                  block
                  x-large
                  style="text-transform: none"
                  @click="e1 = 2"
                >
                  <v-icon left light>mdi-google</v-icon> Google Calendar から追加
                </v-btn>
              </div>
              <div class="my-5">
                <v-btn
                  block
                  x-large
                  style="text-transform: none"
                  @click="e1 = 2"
                >
                <v-icon left light>mdi-apple</v-icon> iCloud Calendar から追加
                </v-btn>
              </div>
              <div class="my-5">
                <v-btn
                  block
                  x-large
                  style="text-transform: none"
                  @click="e1 = 2"
                >
                <v-icon left light>mdi-microsoft</v-icon> Outlook Calendar から追加
                </v-btn>
              </div>
              <div class="my-5">
                <v-divider></v-divider>
              </div>
              <div class="my-5">
                <v-btn
                  block
                  x-large
                  style="text-transform: none"
                  @click="e1 = 2"
                >
                  icalのURLから手動で追加
                </v-btn>
              </div>
              <div class="my-5">
                利用したいサービスが一覧にない場合、ical形式のURLを用いたカレンダーの手動追加をお試しください。
              </div>
            </div>

            <v-btn text>
              キャンセル
            </v-btn>
          </v-stepper-content>

          <v-stepper-content step="2">
            <p>以下のカレンダーが見つかりました。必要なカレンダーを選択してください。</p>

            <div class="my-5">
              <v-list-item-group
                multiple
                active-class=""
              >
                <v-list>
                  <v-list-item>
                    <template v-slot:default="{ active }">
                      <v-list-item-avatar>
                        <v-icon left>mdi-calendar</v-icon>
                      </v-list-item-avatar>
                      <v-list-item-content>
                        <v-list-item-title>ほげほげカレンダー</v-list-item-title>
                      </v-list-item-content>
                      <v-list-item-action>
                        <v-checkbox :input-value="active"></v-checkbox>
                      </v-list-item-action>
                    </template>
                  </v-list-item>
                </v-list>
              </v-list-item-group>
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
            <p>選択されたカレンダーのデフォルトの権限設定を行ってください。</p>

            <div class="my-5">
              <v-list>
                <ListItemCalenderPermission />
                <ListItemCalenderPermission />
                <ListItemCalenderPermission />
              </v-list>
            </div>

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
  name: 'NewCalendarPage',
  layout: 'app',
  data () {
      return {
        e1: 1,
      }
  }
}
</script>
