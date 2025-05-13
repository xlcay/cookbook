<script setup>
import tarifler from '~/data/tarifler.json'
import { useRoute } from 'vue-router'

const route = useRoute()
const id = route.params.id

const tarif = tarifler.find(t => String(t.id) === id)

</script>

<template>
  <div class="p-4 max-w-xl mx-auto">
    <h1 class="text-2xl font-bold mb-4">{{ tarif.baslik }}</h1>
    <img :src="tarif.resim" class="w-full h-64 object-cover mb-4 rounded-3xl" />
    
    <div>
      <h2 class="text-lg font-semibold mb-2">Malzemeler</h2>
      <ul class="list-disc pl-6 mb-4">
        <li v-for="m in tarif.malzemeler" :key="m">{{ m }}</li>
      </ul>

      <h2 class="text-lg font-semibold mb-2">Hazırlanışı</h2>
      <ol class="list-decimal pl-6">
        <li v-for="adim in tarif.hazirlanis" :key="adim">{{ adim }}</li>
      </ol>
      <h2 class="mt-4 text-base font-bold text-gray-700">{{ tarif.notlar }}</h2>
        <NuxtLink to="/" class="inline-block px-4 py-2 m-4 rounded-full bg-green-500 text-white text-sm hover:bg-green-600 transition">
        Ana Sayfaya Dön
      </NuxtLink>
    </div>
    
  </div>
</template>
