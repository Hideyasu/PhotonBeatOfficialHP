<script>
  let tickets = [
    { time: "14:30", stage: "MAIN STAGE", team: "Team A", price: "FREE" }, 
    { time: "14:35", stage: "MAIN STAGE", team: "Team B", price: "FREE" }, 
    { time: "14:40", stage: "MAIN STAGE", team: "Team C", price: "FREE" }, 
    { time: "14:45", stage: "MAIN STAGE", team: "Team D", price: "FREE" }, 
    { time: "14:50", stage: "MAIN STAGE", team: "Team E", price: "FREE" }, 
    { time: "14:55", stage: "MAIN STAGE", team: "Team F", price: "FREE" }, 
    { time: "15:00", stage: "MAIN STAGE", team: "Team G", price: "FREE" }, 
    { time: "15:05", stage: "MAIN STAGE", team: "Team H", price: "FREE" }, 
    { time: "15:10", stage: "MAIN STAGE", team: "Team I", price: "FREE" },  
  ];
</script>

<div class="min-h-screen bg-black text-white font-sans relative overflow-hidden">

  <!-- Hero Section -->
  <section
    class="relative h-screen bg-cover bg-center bg-fixed flex items-center justify-center"
    style="background-image: url('/hero-bg.jpg')"
  >
    <div class="absolute inset-0 bg-black/60"></div>
    <div class="relative z-10 text-center text-white">
      <h1 class="text-6xl md:text-7xl font-extrabold tracking-widest drop-shadow-[0_0_25px_#ff00ff]">
        THE EPIPHANY MOMENT
      </h1>
    </div>
  </section>

  <!-- Musical Journey & Immersive -->
  <section class="max-w-7xl mx-auto py-16 grid md:grid-cols-2 gap-12 px-6">
    <!-- Musical Journey -->
    <div class="bg-white/5 backdrop-blur-sm p-6 rounded-xl border border-purple-600 shadow-[0_0_20px_#9f7aea]">
      <h2 class="text-2xl font-bold mb-6">MUSICAL JOURNEY</h2>
      <ul class="space-y-3 text-gray-300">
        <li class="flex items-center gap-3"><span class="w-3 h-3 bg-cyan-400 rounded-full shadow-[0_0_6px_#00ffff]"></span> Echog floorflows</li>
        <li class="flex items-center gap-3"><span class="w-3 h-3 bg-red-500 rounded-full shadow-[0_0_6px_#ff0000]"></span> Echoes & Tomorrow</li>
        <li class="flex items-center gap-3"><span class="w-3 h-3 bg-green-400 rounded-full shadow-[0_0_6px_#00ff00]"></span> Syntenagtic Harmonies</li>
        <li class="flex items-center gap-3"><span class="w-3 h-3 bg-yellow-400 rounded-full shadow-[0_0_6px_#ffff00]"></span> Syntettic Harmonies</li>
      </ul>
    </div>

    <!-- Immersive -->
    <div class="bg-white/5 backdrop-blur-sm p-6 rounded-xl border border-pink-600 shadow-[0_0_20px_#ec4899]">
      <h2 class="text-2xl font-bold mb-6">IMMERSIVE EXPERIENCE</h2>
      <div class="grid grid-cols-2 gap-6">

        <!-- 1枚目 -->
        <div class="bg-purple-800/40 border border-purple-400 p-4 rounded-lg hover:scale-105 transition shadow-[0_0_15px_#a78bfa] flex flex-col items-center">
          <img src="/a1.png" alt="Immersive Visual 1" class="rounded mb-3 w-24 h-24 object-cover" />
          <p class="text-sm">Immersive Visual 1</p>
        </div>

        <!-- 2枚目 -->
        <div class="bg-pink-800/40 border border-pink-400 p-4 rounded-lg hover:scale-105 transition shadow-[0_0_15px_#f472b6] flex flex-col items-center">
          <img src="/a2.png" alt="Immersive Visual 2" class="rounded mb-3 w-24 h-24 object-cover" />
          <p class="text-sm">Immersive Visual 2</p>
        </div>

      </div>
    </div>
  </section> <!-- ←ここで閉じるのが大事！ -->

  <!-- CREATOR -->
  <section class="max-w-7xl mx-auto py-16 px-6">
    <h2 class="text-2xl font-bold mb-6">CREATOR</h2>
    <div class="grid grid-cols-2 md:grid-cols-4 gap-6">

      <div class="relative overflow-hidden rounded-lg shadow-[0_0_20px_#ec4899]">
        <img src="/hideyasu.png" alt="HIDEYASU YAMAGUCHI" class="w-full h-70 object-cover" />
        <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-transparent flex items-end p-3 text-lg font-bold">
          HIDEYASU YAMAGUCHI
        </div>
      </div>

      <div class="relative overflow-hidden rounded-lg shadow-[0_0_20px_#06b6d4]">
        <img src="/tomoro.png" alt="TOMORO HAYASHI" class="w-full h-70 object-cover" />
        <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-transparent flex items-end p-3 text-lg font-bold">
          TOMORO HAYASHI
        </div>
      </div>

      <div class="relative overflow-hidden rounded-lg shadow-[0_0_20px_#a855f7]">
        <img src="/takahiro.png" alt="TAKAHIRO FUJII" class="w-full h-70 object-cover" />
        <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-transparent flex items-end p-3 text-lg font-bold">
          TAKAHIRO FUJII
        </div>
      </div>

    </div>
  </section>

  <!-- SCHEDULE -->
  <section class="max-w-7xl mx-auto py-16 px-6">
    <h2 class="text-2xl font-bold mb-6">SCHEDULE</h2>
   <table class="w-full table-fixed border-collapse">
  <thead>
    <tr class="text-gray-400 border-b border-gray-600">
      <th class="pb-3 w-1/4 text-center">TIME</th>
      <th class="pb-3 w-1/4 text-center">STAGE</th>
      <th class="pb-3 w-1/4 text-center">TEAM</th>
      <th class="pb-3 w-1/4 text-center">TICKET</th>
    </tr>
  </thead>
  <tbody>
    {#each tickets as t}
      <tr class="border-t border-gray-700 hover:bg-white/5 transition">
        <td class="py-3 text-center">{t.time}</td>
        <td class="text-center">{t.stage}</td>
        <td class="text-center">{t.team}</td>
        <td class="text-center">
          <span class="px-3 py-1 rounded bg-yellow-400 text-black font-bold shadow-[0_0_10px_#ffff00]">
            {t.price}
          </span>
        </td>
      </tr>
    {/each}
  </tbody>
</table>


  </section>

</div>
STAGEを右に寄せたいコードお願い

