<template>
 <Navbar />
 <div class="flex flex-col items-center justify-center">
  <img class="w-32 h-32" src="/cartoonavatar.png">
  <div class="flex gap-5 p-5">
    <div class="relative">
      <input class="w-full pr-16 py-2 text-xs outline outline-green-500/20 rounded-full pl-4" type="text" placeholder="Hangi Tarifi İstersin?"></input>
      <button class="absolute right-1 top-1 bottom-1 px-4 rounded-full bg-green-500 hover:transition hover:duration-200 hover:ease-out hover:bg-green-200 text-[10px] p-1">Ara</button>
    </div>
    <button class="rounded-3xl bg-green-500 hover:transition hover:duration-200 hover:ease-out hover:bg-green-200 text-[10px] p-2">Rastgele</button>
  </div>
 </div>

 <div class="grid xs:grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-5 xs:gap-2 xs:px-2 gap-4 p-4">
  <div class="xs:overflow-hidden line-clamp-1 hover:line-clamp-none hover:h-auto md:w-48 md:h-48 sm:w-36 sm:h-36 xs:w-40 xs:h-40 bg-white rounded-xl shadow hover:shadow-lg hover:transition hover:duration-1000 hover:ease-out">
    <img src="/pogaca.jpeg" loading="lazy" alt="Tarif Görseli" class="w-full h-24 object-cover rounded-t-xl">
    <div class="p-2">
      <h3 class="text-lg xs:font-medium font-semibold mb-1">Peynirli Poğaça</h3>
      <p  class="xs:hidden text-sm text-gray-600">Yumuşacık hamuruyla klasik bir poğaça tarifi. İçinde bol peynir var!</p>
    </div>
  </div>
  <div class="xs:overflow-hidden line-clamp-1 hover:line-clamp-none hover:h-auto md:w-48 md:h-48 sm:w-36 sm:h-36 xs:w-40 xs:h-40 bg-white rounded-xl shadow hover:shadow-lg hover:transition hover:duration-1000 hover:ease-out">
    <img src="/anayemek.png" loading="lazy" alt="Tarif Görseli" class="w-full h-24 object-cover rounded-t-xl">
    <div class="p-2">
      <h3 class="text-lg xs:font-medium font-semibold mb-1">Şinitzel</h3>
      <p  class="xs:hidden text-sm text-gray-600">Yumuşacık hamuruyla klasik bir poğaça tarifi. İçinde bol peynir var!</p>
    </div>
  </div>
  <div class="xs:overflow-hidden line-clamp-1 hover:line-clamp-none hover:h-auto md:w-48 md:h-48 sm:w-36 sm:h-36 xs:w-40 xs:h-40 bg-white rounded-xl shadow hover:shadow-lg hover:transition hover:duration-1000 hover:ease-out">
    <img src="/pogaca.jpeg" loading="lazy" alt="Tarif Görseli" class="w-full h-24 object-cover rounded-t-xl">
    <div class="p-2">
      <h3 class="text-lg xs:font-medium font-semibold mb-1">Peynirli Poğaça</h3>
      <p  class="xs:hidden text-sm text-gray-600">Yumuşacık hamuruyla klasik bir poğaça tarifi. İçinde bol peynir var!</p>
    </div>
  </div>
  <div class="xs:overflow-hidden line-clamp-1 hover:line-clamp-none hover:h-auto md:w-48 md:h-48 sm:w-36 sm:h-36 xs:w-40 xs:h-40 bg-white rounded-xl shadow hover:shadow-lg hover:transition hover:duration-1000 hover:ease-out">
    <img src="/anayemek.png" loading="lazy" alt="Tarif Görseli" class="w-full h-24 object-cover rounded-t-xl">
    <div class="p-2">
      <h3 class="text-lg xs:font-medium font-semibold mb-1">Şinitzel</h3>
      <p  class="xs:hidden text-sm text-gray-600">Yumuşacık hamuruyla klasik bir poğaça tarifi. İçinde bol peynir var!</p>
    </div>
  </div>
  <div class="xs:overflow-hidden line-clamp-1 hover:line-clamp-none hover:h-auto md:w-48 md:h-48 sm:w-36 sm:h-36 xs:w-40 xs:h-40 bg-white rounded-xl shadow hover:shadow-lg hover:transition hover:duration-1000 hover:ease-out">
    <img src="/pogaca.jpeg" loading="lazy" alt="Tarif Görseli" class="w-full h-24 object-cover rounded-t-xl">
    <div class="p-2">
      <h3 class="text-lg xs:font-medium font-semibold mb-1">Peynirli Poğaça</h3>
      <p  class="xs:hidden text-sm text-gray-600">Yumuşacık hamuruyla klasik bir poğaça tarifi. İçinde bol peynir var!</p>
    </div>
  </div>
  <div class="xs:overflow-hidden line-clamp-1 hover:line-clamp-none hover:h-auto md:w-48 md:h-48 sm:w-36 sm:h-36 xs:w-40 xs:h-40 bg-white rounded-xl shadow hover:shadow-lg hover:transition hover:duration-1000 hover:ease-out">
    <img src="/anayemek.png" loading="lazy" alt="Tarif Görseli" class="w-full h-24 object-cover rounded-t-xl">
    <div class="p-2">
      <h3 class="text-lg xs:font-medium font-semibold mb-1">Şinitzel</h3>
      <p  class="xs:hidden text-sm text-gray-600">Yumuşacık hamuruyla klasik bir poğaça tarifi. İçinde bol peynir var!</p>
    </div>
  </div>
</div>

  </template>
  
  <script setup>
import Navbar from '~/components/navbar.vue';
  </script>
  