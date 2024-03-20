<script setup lang="ts">
const features = [
  {
    title: "Easy Note Creation",
    description: "Create new notes quickly and effortlessly.",
  },
  {
    title: "Organize Your Notes",
    description:
      "Organize your notes into categories and tags for easy retrieval.",
  },
  {
    title: "Secure and Private",
    description: "Your notes are securely stored and accessible only to you.",
  },
];

const testimonials = [
  {
    quote:
      "NoteKeeper has revolutionized the way I manage my notes. It's intuitive, easy to use, and highly customizable.",
    author: "John Doe",
  },
  // Add more testimonials here
];
</script>

<template>
  <v-app>
    <!-- Hero Section -->
    <v-container class="hero py-12">
      <v-row align="center" justify="center">
        <v-col cols="12" md="8" lg="6" xl="6">
          <h1 class="text-center mb-4 text-h3">Welcome to NoteKeeper</h1>
          <p class="text-lg text-center mb-8">
            Your one-stop solution for organizing and managing your notes.
          </p>
        </v-col>
      </v-row>
    </v-container>

    <v-container class="cta py-12" fluid>
      <v-row align="center" justify="center">
        <v-col cols="4" class="d-flex align-center justify-center text-none">
          <NuxtLink to="/signup">
            <v-btn
              class="white--text text-none border-none bg-white text-black font-bold"
            >
              Get Started
              <Icon name="ic:baseline-arrow-right-alt" size="1.3rem" />
            </v-btn>
          </NuxtLink>
        </v-col>
      </v-row>
    </v-container>
    <!-- Features Section -->
    <v-container class="features py-12" fluid>
      <h2 class="text-h2 text-center mb-8">Features</h2>
      <v-row align="center" justify="center">
        <v-col
          cols="10"
          md="3"
          v-for="feature in features"
          :key="feature.title"
        >
          <v-card
            variant="elevated"
            class="mx-auto text-center d-flex align-center justify-center"
            min-height="180px"
          >
            <div>
              <v-card-item>
                <div>
                  <div class="text-h6 mb-1">
                    {{ feature.title }}
                  </div>
                  <div class="text-caption">{{ feature.description }}</div>
                </div>
              </v-card-item>
            </div>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>
<style scoped></style>
