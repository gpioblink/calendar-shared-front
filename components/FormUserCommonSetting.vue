<template>
    <v-row>
        <v-col
        cols="12"
        d-flex justify-center
        >
        <v-text-field
            :counter="64"
            label="ユーザー名"
            required
        ></v-text-field>
        </v-col>

        <!-- <v-col
        cols="12"
        d-flex justify-center
        >
        <v-textarea
            :counter="300"
            label="ユーザーの説明"
            required
        ></v-textarea>
        </v-col> -->

        <v-col
        cols="12"
        d-flex justify-center
        >
            <v-select
                :items="['なし','Google','Apple','Microsoft', 'Gravatar']"
                label="アバター画像の取得先"
            ></v-select>
        </v-col>
    </v-row>
                  
</template>