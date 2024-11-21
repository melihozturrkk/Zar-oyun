<template>
  <div id="app" class="text-center">
    <h1>Zar Atma Oyunu</h1>
    <div class="dice" v-if="diceValue !== null">
      <img :src="diceImages[diceValue - 1]" alt="Zar" />
    </div>
    <button @click="rollDice">Zarı At</button>
  </div>
</template>
<script>
import dice1 from '@/assets/dice1.png';
import dice2 from '@/assets/dice2.png';
import dice3 from '@/assets/dice3.png';
import dice4 from '@/assets/dice4.png';
import dice5 from '@/assets/dice5.png';
import dice6 from '@/assets/dice6.png';

export default {
  data() {
    return {
      diceValue: null,
      diceImages: [dice1, dice2, dice3, dice4, dice5, dice6], // Görsel dizisi
    };
  },
  methods: {
    rollDice() {
      this.diceValue = Math.floor(Math.random() * 6) + 1; // 1-6 arası rastgele sayı
    },
  },
};
</script>
<style>
</style>
