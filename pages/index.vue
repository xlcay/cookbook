<template>
 <div class="flex flex-col items-center justify-center">
  <img class="w-32 h-32" src="/cartoonavatar.png">
  <div class="flex gap-5 p-5">
    <div class="relative">
      <input v-model="aramaGirdisi" class="w-full pr-16 py-2 text-xs outline outline-green-500/20 rounded-full pl-4" type="text" placeholder="Hangi Tarifi İstersin?"></input>
        <button @click="aramaYap" class="absolute right-1 top-1 bottom-1 px-4 rounded-full bg-green-500 hover:transition hover:duration-200 hover:ease-out hover:bg-green-200 text-[10px] p-1">Ara</button>
    </div>
    <button @click="rastgeleTarif" class="rounded-3xl bg-green-500 hover:transition hover:duration-200 hover:ease-out hover:bg-green-200 text-[10px] p-2">Rastgele</button>
  </div>
 </div>

 <div class="ml-8 grid xs:grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-5 xs:gap-2 xs:px-2 p-4">
   <div v-for="tarif in filtrelenmisTarifler" :key="tarif.id" class=" xs:overflow-hidden line-clamp-1 hover:line-clamp-none hover:h-auto md:w-64 md:h-64 sm:w-48 sm:h-48 xs:w-32 xs:h-32 bg-white rounded-xl shadow hover:shadow-lg hover:transition hover:duration-1000 hover:ease-out">
        <NuxtLink :to="`/tarifler/${tarif.id}`">
        <img :src="tarif.resim" loading="lazy" alt="Tarif Görseli" class="md:w-full md:h-48 sm:w-full sm:h-48 xs:w-full xs:h-24 object-cover rounded-t-xl">
        <h2 class="text-lg xs:font-medium font-semibold mb-1">{{ tarif.baslik }}</h2>
      </NuxtLink>
    </div>
</div>

  </template>
  
  <script setup>

const { data: tarifler } = await useFetch('/api/tarifler')

const aramaGirdisi = ref('')
const arama = ref('')

const aramaYap = () => {
  arama.value = aramaGirdisi.value
}

const filtrelenmisTarifler = computed(() => {
  const q = arama.value.toLowerCase()
  return tarifler.value?.filter(t => 
    t.baslik.toLowerCase().includes(q) ||
    t.kategori.toLowerCase().includes(q) ||
    t.etiketler.some(e => e.toLowerCase().includes(q))
  ) || []
})

const router = useRouter()

function rastgeleTarif() {
  if (!tarifler.value || tarifler.value.length === 0) return

  const rastgeleIndex = Math.floor(Math.random() * tarifler.value.length)
  const secilen = tarifler.value[rastgeleIndex]
  router.push(`/tarifler/${secilen.id}`)
}
  </script>
  