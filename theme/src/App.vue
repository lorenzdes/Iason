<!-- eslint-disable vue/no-parsing-error -->
<!-- eslint-disable max-len -->
<template>
  <v-app>
    <v-app-bar>
      <v-container class="d-flex align-center py-0">
        <v-app-bar-title class="pl-0">
          <div class="d-flex align-center">
            <v-avatar
              class="me-3"
              :image="'https://www.bing.com/th?id=OIP.wiMDLxoYA1B3WxyzsaNS8gHaHx&w=150&h=157&c=8&rs=1&qlt=90&o=6&dpr=1.7&pid=3.1&rm=2'"
              rounded="0"
            />

            The group
          </div>
        </v-app-bar-title>

        <v-spacer />

        <v-btn-alt
          append-icon="mdi-open-in-new"
          href="https://technesthai.com/about.html"
          rel="noopener noreferrer"
          target="_blank"
          text="About Technestai"
        />
      </v-container>
    </v-app-bar>

    <v-main>
      <section id="hero">
        <v-sheet
          class="d-flex align-center pb-16"
          color="grey-darken-3"
        >
          <v-container class="text-center">
            <v-responsive class="mx-auto" width="500">
              <v-img
                src="https://www.bing.com/th?id=OIP.wiMDLxoYA1B3WxyzsaNS8gHaHx&w=150&h=157&c=8&rs=1&qlt=90&o=6&dpr=1.7&pid=3.1&rm=2"
                height="400"
              />

              <h3 class="text-h3">
                Try the group
              </h3>

              <p class="mt-4 text-medium-emphasis">
                This is a basic Vuetify 3 application designed to help in the understanding of the group Technestai and iasonltd
              </p>
            </v-responsive>
          </v-container>
        </v-sheet>
      </section>

      <v-sheet class="py-16">
        <section id="filter">
          <v-container>
            <v-row justify="space-between">
              <v-col cols="auto">
                <v-responsive width="350">
                  <h2 class="text-h4">
                    Risk, compliance, value
                  </h2>

                  <p class="text-success mt-3">
                    Service for financial institutions
                  </p>

                  <strong class="mt-3">
                    Financial services
                  </strong>

                  <p class="mt-8">
                    We employ powerful analytics and advanced tools to better assess the risks of products in your Banking and Trading Book and provide smart solutions to support you in your measurement and management process.                  </p>

                  <p class="mt-8">
                    All our solutions are designed along regulatory guidelines and completely documented to better support your Institution in the audit process and for any requests from the National and International Supervisor Authorities.                  </p>

                  <v-btn
                    class="mt-6"
                    href="https://www.iasonltd.com/"
                    target="_blank"
                    rel="noopener noreferrer"
                  >
                    More Information
                  </v-btn>
                </v-responsive>
              </v-col>

              <v-img
                max-width="400"
                src="https://th.bing.com/th/id/OIP.L8Cvfm0iM03hzltC6aC6bQAAAA?rs=1&pid=ImgDetMain"
              />
            </v-row>
          </v-container>
        </section>

        <v-container>
          <v-divider class="my-12" />
        </v-container>
        <v-container>
          <v-row justify="center">
            <v-col cols="12" md="6">
              <v-select
                v-model="selectedOption"
                :items="options"
                label="Select an Option"
              />
            </v-col>
          </v-row>
          <!-- Display Wikipedia link based on selected option -->
          <v-row v-if="selectedOption">
            <v-col class="text-center">
              <a :href="getWikipediaLink(selectedOption)" target="_blank" rel="noopener noreferrer">
                Learn more on Wikipedia
              </a>
            </v-col>
          </v-row>
        </v-container>
        <section id="controls">
          <v-container>
            <v-row justify="space-between">
              <v-col cols="auto">
                <v-responsive width="350">
                  <h2 class="text-h4">
                    IT Consulting, Financial and Management software
                  </h2>

                  <p class="text-success mt-3">
                    Tech solutions for the financial sector
                  </p>

                  <p class="mt-3">
                    We are a young company committed to provide technological support to financial companies. We help companies to improve their efficency and agility with bespoken technology ecosystems aimed at costs reduction.                   </p>

                  <p class="mt-8">
                    Our solutions range from Artificial Intelligence and Machine Learning researches to the implementation of custom web applications. We help answering the fast changing technological needs of the financial sector.
                  </p>

                  <v-btn
                    class="mt-6"
                    href="https://technesthai.com/"
                    rel="noopener noreferrer"
                    target="_blank"
                  >
                    More Information
                  </v-btn>
                </v-responsive>
              </v-col>

              <v-img
                max-width="400"
                src="https://th.bing.com/th/id/OIP.E-ZK9pgeACk9k33Im65f2gHaFj?rs=1&pid=ImgDetMaing"
              />
            </v-row>
          </v-container>
        </section>

        <v-container>
          <v-divider class="my-12" />
        </v-container>
      </v-sheet>
    </v-main>

    <v-footer>
      <v-container class="text-overline d-flex align-center justify-space-between">
        <div>
          Copyright &copy; 2016-{{ (new Date()).getFullYear() }} Vuetify, LLC
        </div>

        <v-icon icon="$vuetify" size="x-large" />
      </v-container>
    </v-footer>
  </v-app>
</template>

<script setup>
  import { ref } from 'vue'

  // Define the options
  const options = ['Risk', 'Trading', 'Financial Accounting']

  // Define the selected option
  const selectedOption = ref(null)

  // Method to get Wikipedia link based on selected option
  const getWikipediaLink = option => {
    switch (option) {
      case 'Risk':
        return 'https://en.wikipedia.org/wiki/Risk'
      case 'Trading':
        return 'https://en.wikipedia.org/wiki/Trading'
      case 'Financial Accounting':
        return 'https://en.wikipedia.org/wiki/Financial_accounting'
      default:
        return ''
    }
  }
</script>
