<template>
    <v-row justify="center">
      <v-col cols="12">
        <v-card>
          <v-card-title>ルームオーナー向け設定画面</v-card-title>
          <v-card-text>
            ルームの設定内容の変更ができます。

            <FormRoomCommonSetting />

             <v-divider class="my-4"></v-divider>

             <p>ルームに関する重要な設定ができます。</p>

             <v-btn outlined color="red">オーナー権限を移行</v-btn>
             <v-btn outlined color="red">ルームを削除</v-btn>

          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </template>
  
  <script>
  export default {
    name: 'RoomAdminPage',
    layout: 'room'
  }
  </script>