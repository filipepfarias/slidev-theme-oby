<template>
  <div class="slidev-layout cover">
    <!-- Background image / emblem -->
    <div class="absolute bottom--120 left-10 z-0 w-1/2 h-2/1">
      <img src="../assets/brasao4_vertical_white.svg" class="object-contain w-full h-full opacity-15" />
    </div>

    <!-- Main content -->
    <div class="flex flex-col justify-around h-full relative z-10">
      <div>
        <span class="font-serif font-light text-size-3" v-html="$slidev.configs.event" />
      </div>
      <h1>
        {{ $slidev.configs.title }}
      </h1>
      <div>
        <span class="font-serif font-size-5 font-100">{{ $slidev.configs.author }}</span><br>
        <span class="font-mono font-size-3">{{ $slidev.configs.authorEmail }}</span>
      </div>

      
      <div class="font-serif font-100 text-4">
        {{ $slidev.configs.department }}<br>
        {{ $slidev.configs.institution }}
      </div>
      
      <div>
        23 July, 2025
      </div>
      
      <div>
        <slot />
      </div>

      <!-- Logos row -->
      <div class="flex justify-around items-center mt-4" style="height: 90px; margin: 0 80pt;">
        <img class="h-11 max-h-full max-w-full pr-5" src="../assets/DETI_horizontal_branco.png" />
        <img class="h-22 max-h-full max-w-full" src="../assets/PPGETI_horizontal_branco.svg" />
        <img class="h-34 max-h-full max-w-full" src="../assets/assinatura_UFC70.svg" />
      </div>
    </div>
  </div>
</template>
