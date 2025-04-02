<template>
    <v-container class="py-10">
        <v-row>
            <v-col cols="12" md="8" class="mx-auto">
                <v-card class="pa-5" elevation="5" max-width="600px">
                    <v-card-title class="text-h4 font-weight-bold text-center">Sobre o Sistema Escolar</v-card-title>
                    <v-card-text class="text-body-1 mt-4">
                        Nosso sistema escolar digital foi desenvolvido para modernizar o ensino,
                        substituindo o uso da lousa tradicional por uma plataforma interativa e eficiente.
                        Com ele, alunos e professores têm acesso a recursos inovadores que tornam o aprendizado
                        mais dinâmico e acessível.
                    </v-card-text>
                    <v-divider class="my-4"></v-divider>
                    <v-card-text>
                        <v-list>
                            <v-list-item>
                                <v-list-item-icon>
                                    <v-icon color="primary">mdi-laptop</v-icon>
                                </v-list-item-icon>
                                <v-list-item-content>Aulas interativas e acessíveis</v-list-item-content>
                            </v-list-item>
                            <v-list-item>
                                <v-list-item-icon>
                                    <v-icon color="primary">mdi-cloud-sync</v-icon>
                                </v-list-item-icon>
                                <v-list-item-content>Materiais sempre disponíveis online</v-list-item-content>
                            </v-list-item>
                            <v-list-item>
                                <v-list-item-icon>
                                    <v-icon color="primary">mdi-chart-bar</v-icon>
                                </v-list-item-icon>
                                <v-list-item-content>Acompanhamento do desempenho dos alunos</v-list-item-content>
                            </v-list-item>
                        </v-list>
                    </v-card-text>
                    <v-card-actions class="justify-center">
                        <v-btn color="primary" class="mt-3" @click="goToHome">Voltar para Início</v-btn>
                    </v-card-actions>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    methods: {
        goToHome() {
            this.$router.push('/');
        }
    }
};
</script>

<style scoped>
.v-container {
    max-width: 800px;
}
</style>

<route lang="yaml">
meta:
    requiresAuth: false
    layout: sobre
</route>