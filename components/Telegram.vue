<script setup lang="ts">
import WebApp from '@twa-dev/sdk'

const texts = [
  'У тебя все получится!',
  'Ты справишься!',
  'Ты супер!',
  'Ты лучший!',
  'Ты умница!',
  'Ты космос!',
  'Ты космонавт!',
  'Ты космический корабль!',
  'Ты космический мусор!',
  'Ты космический медведь!',
  'Ты космический кот!',
  'Ты космический пёс!',
  'Ты космический кролик!',
  'Ты космический крокодил!',
  'Ты шиХарен!',
  'Ты шиХаришь!',
  'Ты шиХарище!',
  'Ты крутой!',
  'Ты круче всех!',
  'Ты круче всех крутых!',
  'Ты круче всех крутых крутых!',
  'Ты круче всех крутых крутых крутых!',
  'Ты круче всех крутых крутых крутых крутых!',
  'Ты круче всех крутых крутых крутых крутых крутых!',
  'Ты молодец!',
  'Ты молодчина!',
  'Ты молодчага!',
  'Ты звёздочка!',
  'Ты звезда!',
  'Ты звездочёт!',
  'Ты звездочётка!',
  'Ты звездочёткин!',
  'Ты звездочёткина!',
  'Ты звездочёткинка!',
]

const smileys = [
  '😊',
  '😃',
]

function getHappyText() {
  const text = texts[Math.floor(Math.random() * texts.length)]
  const smiley = smileys[Math.floor(Math.random() * smileys.length)]
  return `${text} ${smiley}`
}
</script>

<template>
<div
  style="
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    overflow: hidden;
    overflow-y: auto;
    text-align: center;
    color: mediumpurple;
    font-size: 44px;
  "
  @click="WebApp.showAlert(getHappyText())"
>
  Привет, {{ WebApp.initDataUnsafe.user?.first_name }}!
  <br/>
  <br/>
  Жмякай<br/>куда<br/>угодно!
</div>
</template>
