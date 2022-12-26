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
          <p>
            一度ルームに登録されたメンバー同士なら、調整ツールなどへの入力を待たず、すぐに日程を確定！
            登録するカレンダーはGoogleやAppleなどical形式での出力が対応していれば何でもOK。
            各人が普段遣いしているカレンダーの情報と同期します。
          </p>
          <p>
            「グループごとにカレンダーの公開範囲の制限」「カレンダーごとに予定あり/微妙/予定なしの指定」など
            細かい権限管理の機能も各種用意しています。普段使いのツールとして、ぜひご利用ください。
          </p>
          <p>
            バグを見つけたら、 <a
              href="https://github.com/vuetifyjs/vuetify/issues"
              target="_blank"
              rel="noopener noreferrer"
              title="contribute"
            >
              GitHubのIssue
            </a>にPRをお願いします。
          </p>
          <div class="text-xs-right">
            <em><small>&mdash; Zliサークル Happy BirthDay チーム一同</small></em>
          </div>
          <hr class="my-3">
          <a
            href="https://nuxtjs.org/"
            target="_blank"
            rel="noopener noreferrer"
          >
            使い方の説明
          </a>
          <br>
          <a
            href="https://github.com/nuxt/nuxt.js"
            target="_blank"
            rel="noopener noreferrer"
          >
            デモ動画
          </a>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn
            color="primary"
            nuxt
            to="/inspire"
          >
            Sign Up
          </v-btn>
        </v-card-actions>
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
