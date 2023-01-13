<template>
    <v-row>
        <v-col
        cols="12"
        d-flex justify-center
        >
        <v-text-field
            :counter="64"
            label="ルーム名"
            required
        ></v-text-field>
        </v-col>

        <v-col
        cols="12"
        d-flex justify-center
        >
        <v-textarea
            :counter="300"
            label="ルームの説明"
            required
        ></v-textarea>
        </v-col>
        <v-col
        cols="12"
        d-flex justify-center
        >
        <v-select
            :items="['なし','Slack','Discord','LINE']"
            label="通知先のアプリ(任意)"
        ></v-select>

        <v-text-field
            label="通知先のURL(任意)"
            ></v-text-field>
        </v-col>
        <v-col
        cols="12"
        d-flex justify-center
        >
        ルームカラー
        <v-color-picker
        ></v-color-picker>
        </v-col>
    </v-row>
                  
</template>