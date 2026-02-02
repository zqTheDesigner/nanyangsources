<template>
  <div>
    <q-dialog v-model="feedbackWindow">
      <q-card>
        <q-card-section>
          <div class="text-h6">Feedback</div>
        </q-card-section>

        <q-card-section class="q-pt-none">
          For feedback and suggestions, please email us at
          <a href="mailto:nanyangsources@gmail.com?subject=Feedback%20for%20Nanyangsources.com"
            >nanyangsources@gmail.com</a
          >
        </q-card-section>

        <q-card-actions align="right">
          <q-btn flat label="OK" color="primary" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>

    <q-footer class="row justify-between no-wrap bg-cyan-10 q-pa-sm text-center">
      <div>© {{ currentYear }}. All rights reserved.</div>
      <div @click="() => (feedbackWindow = true)" class="cursor-pointer">Feedback</div>
    </q-footer>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const currentYear = new Date().getFullYear()
const feedbackWindow = ref(false)
</script>

<style lang="scss" scoped></style>
