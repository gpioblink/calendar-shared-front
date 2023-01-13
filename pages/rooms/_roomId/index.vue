<template>
    <v-row justify="center">
      <v-col cols="12" md="4">
        <v-card>
          <v-card-title>
            ルームのメンバー
          </v-card-title>
          <v-card-text>
            <v-list>
              <ListItemRoomMember />
              <ListItemRoomMember />
              <ListItemRoomMember />
              <ListItemRoomMember />
              <ListItemRoomMember />
              <ListItemRoomMember />
              <ListItemRoomMember />
            </v-list>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="12" md="8">
        <v-card>
          <v-card-title>
            あなたが共有中のカレンダー
          </v-card-title>
          <v-card-text>
            <v-list>
              <ListItemCalenderPermission />
              <ListItemCalenderPermission />
              <ListItemCalenderPermission />
              <ListItemCalenderPermission />
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
              to="schedules/new"
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
  