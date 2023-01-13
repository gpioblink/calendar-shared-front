<template>
    <v-row justify="center">
      <v-col cols="12" sm="6">
        <v-card>
          <v-card-title>日程調整用カレンダーを開く</v-card-title>
          <v-card-subtitle>〇〇時に作成された、〇〇,〇〇,〇〇のユーザーとの日程調整用カレンダーが準備できています。開く方法を選択し、日程調整を行ってください。</v-card-subtitle>
          <v-card-text>
            <ButtonGroupCalendarOpen />
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </template>

    
<script>
export default {
  name: 'ScheduleOpenPage',
  layout: 'room'
}
</script>