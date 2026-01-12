<template>
  <v-app>
    <v-main>
      <v-container class="text-center mt-10">
        <h1 class="text-h4 font-weight-bold mb-4">Nuxt + Vuetify 動作確認ページ</h1>
        <v-btn color="primary" @click="toggleDark">
          <v-icon start>mdi-theme-light-dark</v-icon>
          Toggle Dark Mode
        </v-btn>
      </v-container>
    </v-main>
  </v-app>
</template>

<script setup>
import { useTheme } from 'vuetify'

const theme = useTheme()

const toggleDark = () => {
  const current = theme.global.name.value
  const next = current === 'light' ? 'dark' : 'light'
  theme.change(next)
}
</script>
