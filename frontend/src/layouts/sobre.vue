<template>
    <v-app theme="light">
        <v-card class="pa-4">
            <v-card-text>
                <router-view></router-view>
            </v-card-text>
        </v-card>
    </v-app>
</template>

<script lang="ts">
export default {
    name: 'LoginLayout'
}
</script>