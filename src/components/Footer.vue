<script setup lang="ts">
import { useI18n } from 'vue-i18n'
import { isDark, toggleDark } from '~/logic'

const { t, availableLocales, locale } = useI18n()

const toggleLocales = () => {
  // change to some real logic
  const locales = availableLocales
  locale.value = locales[(locales.indexOf(locale.value) + 1) % locales.length]
}
</script>

<template>
  <nav class="navid text-xl mt-6">
    <router-link class="icon-btn mx-2" to="/" :title="t('button.home')">
      <ri:firefox-fill />
    </router-link>

    <a class="aikon-theme icon-btn mx-2" :title="t('button.toggle_dark')" @click="toggleDark">
      <bi:moon-stars v-if="isDark" />
      <carbon-sun v-else />
    </a>

    <a class="aikon-translate icon-btn mx-2" :title="t('button.toggle_langs')" @click="toggleLocales">
      <vs:language />
    </a>

    <router-link class="icon-btn mx-2" to="/about" :title="t('button.about')">
      <fluent:calendar-question-mark-16-regular />
    </router-link>

    <a class="icon-btn mx-2" rel="noreferrer" href="https://gitlab.com/AifoxHi/aifoxhi.tk-website" target="_blank" title="GitHub">
      <fa:gitlab />
    </a>
  </nav>
</template>
