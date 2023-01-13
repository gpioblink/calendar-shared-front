<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card>
        <v-card-title class="headline">
          ようこそ
        </v-card-title>
        <v-card-text>
          <p>みんなのカレンダーは、各人が自分の持つ全てのカレンダーを登録しておいて、
            友達やサークル等のグループ全員で共有できるツールです。
          </p>
          <v-row class="my-6">
              <v-btn color="primary" class="mx-auto" to="/user/signup">さっそくはじめる</v-btn>
          </v-row>
          <v-row class="my-4">
              <v-btn class="mx-auto" to="/user/login">ログイン</v-btn>
          </v-row>
        </v-card-text>

      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'IndexPage',
  layout: 'app'
}
</script>
