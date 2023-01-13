<template>
    <v-row justify="center" align="center">
      <v-col cols="12" xs5>
        予定の調整
      </v-col>
      <v-col cols="12">
        <v-stepper v-model="e1">
          <v-stepper-header>
            <v-stepper-step
              :complete="e1 > 1"
              step="1"
            >
              予定調整するメンバーの選択
            </v-stepper-step>

            <v-divider></v-divider>
  
            <v-stepper-step
              :complete="e1 > 2"
              step="2"
            >
              予定の作成
            </v-stepper-step>
          </v-stepper-header>
  
          <v-stepper-items>
            <v-stepper-content step="1">
  
              <p>予定を調整したいメンバーを全て選択してください。</p>

              <v-list>
                <v-list-item
                ripple
                >
                <v-list-item-action>
                    <v-icon :color="1 > 0 ? 'indigo darken-4' : ''">
                    mdi-minus-box
                    </v-icon>
                </v-list-item-action>
                <v-list-item-content>
                    <v-list-item-title>
                    全て選択
                    </v-list-item-title>
                </v-list-item-content>
                </v-list-item>
                <v-divider class="my-2"></v-divider>
                
                <ListItemMemberWithCheckBox />
                <ListItemMemberWithCheckBox />
                <ListItemMemberWithCheckBox />
                <ListItemMemberWithCheckBox />
                <ListItemMemberWithCheckBox />
                <ListItemMemberWithCheckBox />
              </v-list>

 
              <v-btn
                color="primary"
                class="my-2"
                @click="e1 = 2"
              >
                次へ
              </v-btn>
              
              <v-btn text>
                キャンセル
              </v-btn>
            </v-stepper-content>
  
            <v-stepper-content step="2">
              <p>日程調整用のカレンダーが作成されました。カレンダーを確認して日程を確定させてください。</p>

              <ButtonGroupCalendarOpen />

            </v-stepper-content>
          </v-stepper-items>
        </v-stepper>
      </v-col>
    </v-row>
  </template>
  
  <script>
  export default {
    name: 'NewSchedulePage',
    layout: 'room',
    data () {
        return {
          e1: 1,
        }
    }
  }
  </script>
  