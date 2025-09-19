<script setup>
const nav = $slidev.nav
const configs = $slidev.configs
</script>

<template>
  <Transition name="fade" mode="out-in">
    <div
      v-if="nav.currentPage > 1"
      absolute w-full flex justify-between items-center px-4 font-serif font-400 text-xs text-gray-500 z-50 
    >
      <div>{{ $slidev.configs.event }}</div>
      <div>
        <img src="./assets/assinatura_conjunta_horizontal_monocromatica.svg" class="max-h-10 filter invert dark:invert-0"></img>
      </div>
    </div>
  </Transition>
  <Transition name="fade" mode="out-in">
    <div
      v-if="nav.currentPage > 1"
      absolute text-size-3 bottom-0 left-0 w-full flex justify-between items-center px-4 py-2 text-gray-500 z-50 
    >
      <div>{{ $slidev.configs.shortAuthor ?? $slidev.configs.author }}</div>
      <div>{{ $slidev.configs.shortTitle ?? $slidev.configs.title }}</div>
      <div> {{ nav.currentPage }} / {{ nav.total }}</div>
    </div>
  </Transition>
</template>