<template>
    <v-app theme="light">
        <v-container class="fill-height align-center justify-center">
            <v-card class="pa-4">
                <v-card-text>
                    <router-view></router-view>
                </v-card-text>
            </v-card>
        </v-container>
    </v-app>
</template>

<script lang="ts">
export default {
    name: 'LoginLayout'
}
</script>