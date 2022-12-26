<template>
  <v-row justify="center">
    <v-col cols="12">
      <v-card>
        <v-card-title>〇〇さん、みんなのカレンダーへようこそ！</v-card-title>
        <v-card-subtitle>
          <p>今日はどんな予定を立てますか？ 「所属ルーム」から、予定を調整したい団体を選んで、開始ボタンを押してください。</p>
        </v-card-subtitle>
      </v-card>
    </v-col>


    <v-col cols="12" md="6">
      <v-card>
        <v-card-title>
          所属ルーム
        </v-card-title>
        <v-card-subtitle>
          
          <div align="left">
            <v-btn
                color="secondary"
                outlined
              >
                <v-icon>mdi-plus</v-icon>
                ルーム作成
            </v-btn>

            <v-btn
                color="secondary"
                outlined
              >
                <v-icon>mdi-plus</v-icon>
                招待コードから参加
            </v-btn>

          </div>
        </v-card-subtitle>
        <v-card-text>
          カレンダーアイコンを押すと予定の調整を開始します。
          <v-list>            
            <ListItemRoom />  
            <ListItemRoom />  
            <ListItemRoom />  
            <ListItemRoom />  
            <ListItemRoom />  
            <ListItemRoom />  
            <ListItemRoom />  
            <ListItemRoom />  
            <ListItemRoom />  
            <ListItemRoom />  
            <ListItemRoom />  
            <ListItemRoom />  
            <ListItemRoom />  
            <ListItemRoom />
          </v-list>
        </v-card-text>
      </v-card>
    </v-col>

    <v-col cols="12" md="6">
      <v-card>
        <v-card-title>
          登録済みカレンダー
        </v-card-title>
        <v-card-subtitle>
          <div align="left">
            <v-btn
                color="secondary"
                outlined
              >
                <v-icon>mdi-plus</v-icon>
                カレンダーの追加
            </v-btn>
          </div>
        </v-card-subtitle>
        <v-card-text>
          デフォルトの公開範囲の設定が行えます。
          <v-list>            
            <ListItemCalenderPermission />
            <ListItemCalenderPermission />
            <ListItemCalenderPermission />
            <ListItemCalenderPermission />
            <ListItemCalenderPermission />
            <ListItemCalenderPermission />
            <ListItemCalenderPermission />
            <ListItemCalenderPermission />
          </v-list>
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
