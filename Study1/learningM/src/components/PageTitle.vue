<template>
    <v-container class="mk-page-title">
      <div class="d-flex align-center">
        <slot name="left"></slot>
        <v-tooltip top>
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              v-if="previousLocation === true"
              class="mr-2"
              color="black"
              icon
              large
              v-bind="attrs"
              @click="previousPage"
              v-on="on"
            >
              <v-icon>arrow_back</v-icon>
            </v-btn>
          </template>
          <span>Go Back</span>
        </v-tooltip>
        <div class="page-title flex-grow-1">{{ pageTitle }}</div>
        <slot name="action"></slot>
      </div>
      <v-divider class="mt-4 primary"></v-divider>
    </v-container>
  </template>
  
  <script>
  export default {
    name: "PageTitle",
    props: {
      pageTitle: String,
      previousLocation: {
        type: Boolean,
        default: false,
      },
    },
    methods: {
      async previousPage() {
        await this.$router.go(-1);
      },
    },
  };
  </script>
  
  <style lang="scss">
  .mk-page-title {
    .page-title {
      font-family: "Poppins", "Helvetica", sans-serif !important;
      font-weight: 700 !important;
      font-size: 1.5rem;
    }
  }
  </style>