<script setup lang="ts">
type Job = {
  company: string;
  website: string;
  location: string;
  from: string;
  to: string;
  title: string;
  description: string;
  stack: {
    name: string;
  }[];
};

const details = defineProps<Job>();

function openWebsite() {
  window.location.href = details.website;
}

function toMonthNameYear(dateStr: string): string {
    if(dateStr == "PRESENT"){
      return "Present";
    }

    if (!/^\d{8}$/.test(dateStr)) {
        throw new Error("Invalid date format. Expected yyyymmdd.");
    }

    const year = parseInt(dateStr.slice(0, 4), 10);
    const month = parseInt(dateStr.slice(4, 6), 10) - 1; // Months are 0-indexed
    const day = parseInt(dateStr.slice(6, 8), 10);

    const date = new Date(year, month, day);

    if (isNaN(date.getTime())) {
        throw new Error("Invalid date.");
    }

    const options: Intl.DateTimeFormatOptions = { month: 'short', year: 'numeric' };
    return date.toLocaleDateString('en-US', options);
}
</script>

<template>
  <v-hover v-slot="{ isHovering, props }">
    <v-card
      variant="elevated"
      :class="{ 'on-hover': isHovering }"
      v-bind="props"
      link
      @click="openWebsite()"
      color="#65474C"
    >
      <v-container fluid>
        <v-row>
          <v-col class="pt-3 text-right" cols="auto">
            <v-card-subtitle>
              {{ toMonthNameYear(details.from) }} - {{ toMonthNameYear(details.to) }}
            </v-card-subtitle>
          </v-col>
          <v-col class="text-left">
            <v-card-title>
              <a :href="details.website">{{ details.company }}</a>
            </v-card-title>

            <v-card-subtitle>{{ details.location }}</v-card-subtitle>
            <v-card-subtitle>{{ details.title }}</v-card-subtitle>
            <v-card-text>{{ details.description }}</v-card-text>
            <div class="ml-2">
              <v-chip class="ma-1" v-for="(tech, index) in details.stack" :key=index
                >{{ tech.name }}
              </v-chip>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-card>
  </v-hover>
</template>

<style scoped>
.on-hover {
  background-color: rgba(255, 255, 255, 0.8);
}
</style>
