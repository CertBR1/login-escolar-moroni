<template>
    <v-container class="py-10">
        <v-row>
            <v-col cols="12" md="8" class="mx-auto">
                <v-card class="pa-5" elevation="5" max-width="600px">
                    <v-card-title class="text-h4 font-weight-bold text-center">
                        EED - Escola Digital
                    </v-card-title>
                    <v-card-subtitle class="text-h5 font-weight-bold text-center">
                        Nossa politica
                    </v-card-subtitle>
                    <v-card-text class="text-body-1 mt-4">
                        <v-expansion-panels multiple>
                            <v-expansion-panel v-for="(item, index) in regras" :key="index">
                                <v-expansion-panel-title class="font-weight-bold">{{ item.titulo
                                    }}</v-expansion-panel-title>
                                <v-expansion-panel-text>{{ item.descricao }}</v-expansion-panel-text>
                            </v-expansion-panel>
                            <v-divider class="my-4"></v-divider>
                            <v-card-text class="text-body-2 font-italic">
                                Estas políticas visam garantir um ambiente de aprendizado harmonioso e produtivo para
                                todos.
                            </v-card-text>
                        </v-expansion-panels>
                    </v-card-text>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    name: 'SobrePage',
    data: () => ({
        regras: [
            {
                titulo: "1. Respeito e Convivência",
                descricao:
                    "Todos os alunos, professores e funcionários devem manter um ambiente de respeito e cordialidade, promovendo um espaço seguro para aprendizado e desenvolvimento pessoal.",
            },
            {
                titulo: "2. Uso de Tecnologia",
                descricao:
                    "O uso de dispositivos eletrônicos é permitido apenas para fins educacionais. O mau uso pode resultar em restrições ou penalidades conforme necessário.",
            },
            {
                titulo: "3. Frequência e Pontualidade",
                descricao:
                    "A presença nas aulas é obrigatória, e atrasos recorrentes podem resultar em medidas disciplinares.",
            },
            {
                titulo: "4. Avaliações e Desempenho",
                descricao:
                    "O desempenho acadêmico será avaliado com base em provas, projetos e participação ativa nas atividades escolares.",
            },
            {
                titulo: "5. Conduta Online",
                descricao:
                    "Todos os alunos devem seguir as diretrizes de uso responsável da internet, evitando conteúdos impróprios e respeitando a privacidade de colegas e professores.",
            },
            {
                titulo: "6. Código de Vestimenta",
                descricao:
                    "A escola pode estabelecer um código de vestimenta adequado ao ambiente educacional, garantindo respeito e profissionalismo.",
            },
            {
                titulo: "7. Penalidades e Advertências",
                descricao:
                    "O descumprimento das políticas pode resultar em advertências, suspensão ou outras medidas cabíveis.",
            },
        ]
    }),
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