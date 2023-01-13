<template>
    <v-row justify="center">
      <v-col cols="12" sm="6">
        <v-card>
          <v-card-title>〇〇ルームに招待されています</v-card-title>
          <v-card-text>
            <CardRoom/>
            <div class="my-4"></div>
            <p>参加してルームメンバーとカレンダーを共有しますか？</p>
            <v-btn color="primary">新規登録して参加</v-btn>
            <v-btn class="mx-3">ログインして参加</v-btn>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </template>
  
  <script>
  export default {
    name: 'RoomInvitePage',
    layout: 'room'
  }
  </script>

<style scoped>
.wrap-text {
   -webkit-line-clamp: unset !important;
}
</style>