<template>
    <v-row justify="center">
      <v-col cols="12">
        <v-card>
          <v-card-title>アカウント連携設定</v-card-title>
          <v-card-text>
            各種カレンダーサービスと連携ができます。
            <v-list two-line>
                <v-list-item>
                    <v-list-item-icon>
                    <v-icon>
                        mdi-google
                    </v-icon>
                    </v-list-item-icon>

                    <v-list-item-content>
                    <v-list-item-title>じぶりん</v-list-item-title>
                    <v-list-item-subtitle>gpionlink@gmail.com</v-list-item-subtitle>
                    </v-list-item-content>

                    <v-list-item-action>
                        <v-row>
                            <v-col><v-btn>連携解除</v-btn></v-col>
                        </v-row>
                    </v-list-item-action>
                </v-list-item>
                
                <v-list-item>
                    <v-list-item-icon>
                    <v-icon>
                        mdi-apple
                    </v-icon>
                    </v-list-item-icon>

                    <v-list-item-content>
                    <v-list-item-title>(iCloud Calendar)</v-list-item-title>
                    <v-list-item-subtitle>未設定</v-list-item-subtitle>
                    </v-list-item-content>

                    <v-list-item-action>
                        <v-row>
                            <v-col><v-btn>連携する</v-btn></v-col>
                        </v-row>
                    </v-list-item-action>
                </v-list-item>
                

                <v-list-item>
                    <v-list-item-icon>
                    <v-icon>
                        mdi-microsoft
                    </v-icon>
                    </v-list-item-icon>

                    <v-list-item-content>
                    <v-list-item-title>Kai Yamada</v-list-item-title>
                    <v-list-item-subtitle>m5251154@u-aizu.ac.jp</v-list-item-subtitle>
                    </v-list-item-content>

                    <v-list-item-action>
                        <v-row>
                            <v-col><v-btn>連携解除</v-btn></v-col>
                        </v-row>
                    </v-list-item-action>
                </v-list-item>
                

                <v-divider inset></v-divider>

                <v-list-item>
                    <v-list-item-icon>
                    <v-icon>
                        mdi-email
                    </v-icon>
                    </v-list-item-icon>

                    <v-list-item-content>
                    <v-list-item-title>じぶりん</v-list-item-title>
                    <v-list-item-subtitle>gpionlink@gmail.com</v-list-item-subtitle>
                    </v-list-item-content>

                    <v-list-item-action>
                        <v-row>
                            <v-col><v-btn>変更</v-btn></v-col>
                        </v-row>
                    </v-list-item-action>
                </v-list-item>
             </v-list>
             <v-divider class="my-4"></v-divider>

             <p>アカウントに関する重要な設定ができます。</p>

             <v-btn outlined color="red">アカウントを削除</v-btn>

          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </template>
  
  <script>
  export default {
    name: 'UserIntegrationPage',
    layout: 'app'
  }
  </script>