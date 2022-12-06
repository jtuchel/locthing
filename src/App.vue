<script setup lang="ts">
import { useLocale } from 'vuetify'
import { useI18n } from 'vue-i18n'

const { current } = useLocale()
const { t } = useI18n()

setTimeout(() => {
  current.value = 'de';
}, 3000);
</script>

<template>
  <div>
    <div>content:</div>
    <div>{{ t('title') }}</div>
  </div>
</template>

<i18n>
  {
    "en": {
      "title": "title | en"
    },
    "de": {
      "title": "Titel | de"
    }
  }
</i18n>