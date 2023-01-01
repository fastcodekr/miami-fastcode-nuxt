<template>
  <v-container class="max-lg footer">
    <v-row class="spacing4">
      <v-col
        class="pa-4"
        md="3"
        cols="12"
      >
        <div class="logo">
          
          <h6 class="title">
            <!--{{ brand.agency.projectName }} -->
          </h6>
        </div>
        <p class="footer-desc pb-2">
          <!--{{ $t('agencyLanding.footer_paragraph') }}-->
        </p>
       
      </v-col>
      <v-col
        class="pa-6"
        md="6"
        cols="12"
      >
        
      </v-col>
      <v-col
        md="3"
        cols="12"
        class="pa-4"
      >
        <div class="socmed">
          <v-btn
            text
            icon
            class="button"
          >
            <span class="ion-logo-facebook icon" />
          </v-btn>
          <v-btn
            text
            icon
            class="button"
          >
            <span class="ion-logo-twitter  icon" />
          </v-btn>
          <v-btn
            text
            icon
            class="button"
          >
            <span class="ion-logo-instagram icon" />
          </v-btn>
          <v-btn
            text
            icon
            class="button"
          >
            <span class="ion-logo-linkedin icon" />
          </v-btn>
        </div>
        <v-select
          :items="langList"
          :value="lang"
          v-model="lang"
          label=""
          outlined
          class="select-lang"
          prepend-inner-icon="mdi-web"
          @change="switchLang(lang)"
        />
      </v-col>
    </v-row>

  </v-container>
</template>

<style scoped lang="scss">
@import './footer-style';
</style>

<script>

export default {
  data: () => ({
   
    lang: 'en',
    footers: [
      {
        title: 'Company',
        description: ['Team', 'History', 'Contact us', 'Locations'],
        link: ['#team', '#history', '#contact-us', '#locations']
      },
      {
        title: 'Resources',
        description: [
          'Resource',
          'Resource name',
          'Another resource',
          'Final resource'
        ],
        link: [
          '#resource',
          '#resource-name',
          '#another-resource',
          '#final-resource'
        ]
      },
      {
        title: 'Legal',
        description: ['Privacy policy', 'Terms of use'],
        link: ['#privacy-policy', '#terms-of-use']
      }
    ]
  }),
  computed: {
    
    langList: function() {
      const list = []
      return list
    }
  },
  mounted() {
    
  },
  methods: {
    
  }
}
</script>
