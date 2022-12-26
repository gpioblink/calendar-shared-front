<template>
    <v-row justify="center">
      <v-col cols="12" sm="6" md="4">
        <v-card>
          <v-card-title>
            ルームのメンバー
          </v-card-title>
          <v-card-text>
            <v-list>
              <v-list-item
              >
                <v-list-item-avatar>
                  <v-icon
                    class="grey lighten-1"
                    dark
                  >
                  mdi-account
                  </v-icon>
                </v-list-item-avatar>
  
                <v-list-item-content>
                  <v-list-item-title>じぶりん</v-list-item-title>
                </v-list-item-content>
  
                <v-list-item-action>
                    <v-btn icon><v-icon>mdi-cancel</v-icon></v-btn>
                </v-list-item-action>
              </v-list-item>

              <v-list-item
              >
                <v-list-item-avatar>
                  <v-icon
                    class="grey lighten-1"
                    dark
                  >
                  mdi-account
                  </v-icon>
                </v-list-item-avatar>
  
                <v-list-item-content>
                  <v-list-item-title>npJxx</v-list-item-title>
                </v-list-item-content>
  
                <v-list-item-action>
                    <v-btn icon><v-icon>mdi-cancel</v-icon></v-btn>
                </v-list-item-action>
              </v-list-item>

              <v-list-item
              >
                <v-list-item-avatar>
                  <v-icon
                    class="grey lighten-1"
                    dark
                  >
                  mdi-account
                  </v-icon>
                </v-list-item-avatar>
  
                <v-list-item-content>
                  <v-list-item-title>kashu</v-list-item-title>
                </v-list-item-content>
  
                <v-list-item-action>
                    <v-btn icon><v-icon>mdi-cancel</v-icon></v-btn>
                </v-list-item-action>
              </v-list-item>

              <v-list-item
              >
                <v-list-item-avatar>
                  <v-icon
                    class="grey lighten-1"
                    dark
                  >
                  mdi-account
                  </v-icon>
                </v-list-item-avatar>
  
                <v-list-item-content>
                  <v-list-item-title>sou7</v-list-item-title>
                </v-list-item-content>
  
                <v-list-item-action>
                    <v-btn icon><v-icon>mdi-cancel</v-icon></v-btn>
                </v-list-item-action>
              </v-list-item>

              <v-list-item
              >
                <v-list-item-avatar>
                  <v-icon
                    class="grey lighten-1"
                    dark
                  >
                  mdi-account
                  </v-icon>
                </v-list-item-avatar>
  
                <v-list-item-content>
                  <v-list-item-title>tashiro</v-list-item-title>
                </v-list-item-content>
  
                <v-list-item-action>
                    <v-btn icon><v-icon>mdi-cancel</v-icon></v-btn>
                </v-list-item-action>
              </v-list-item>
  
            </v-list>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="12" sm="12" md="8">
        <v-card>
          <v-card-title>
            あなたが共有中のカレンダー
          </v-card-title>
          <v-card-text>
            <v-list>
              <CalenderPermissionSelectorItem />
              <CalenderPermissionSelectorItem />
              <CalenderPermissionSelectorItem />
              <CalenderPermissionSelectorItem />
            </v-list>
          </v-card-text>
        </v-card>
      </v-col>
      <v-btn
              dark
              large
              fixed
              bottom
              right
              color="primary"
              style="z-index: 5;"
              to="/new-room"
            >
              <v-icon>mdi-calendar</v-icon>
              予定の調整を開始
      </v-btn>
    </v-row>
  </template>
  
  <script>
  export default {
    name: 'RoomPage',
    layout: 'room'
  }
  </script>
  