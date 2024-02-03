<script setup lang="ts">
interface Job {
    company: string
    website: string
    location: string
    from: string
    to: string
    title: string
    description: string
    stack: { name: string; }[]
}

const props = defineProps<Job>()
</script>

<template>
    <v-card width="570" :href="props.website" variant="elevated">
        <v-container fluid>
            <v-row no-gutters>
                <v-col class="pt-3 text-right" cols="auto">
                    <v-card-subtitle>
                        {{ props.from }} - {{ props.to }}
                    </v-card-subtitle>
                </v-col>
                <v-col class="text-left">      
                    <v-card-title>
                        <a :href="props.website">{{ props.company }}</a>
                    </v-card-title>

                    <v-card-subtitle>{{ props.location }}</v-card-subtitle>
                    <v-card-subtitle>{{ props.title }}</v-card-subtitle>
                    <v-card-text>{{ props.description }}</v-card-text>
                    <div class="ml-2">
                        <v-chip class="ma-1" v-for="tech in props.stack">{{ tech.name }}</v-chip>
                    </div>
                </v-col>
            </v-row>
        </v-container>
    </v-card>
</template>

<style scoped></style>