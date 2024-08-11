<script setup lang="ts">
import WebApp from '@twa-dev/sdk'

</script>

<template>
<div
  style="
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    color: mediumpurple;
    font-size: 44px;
  "
  @click="WebApp.showAlert('У тебя все получится!')"
>
  Жмякай по мне!
</div>
</template>
