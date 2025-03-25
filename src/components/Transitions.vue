<template>
    <div class="card-grid">
      <div
        v-for="card in cards"
        :key="card.id"
        class="card-wrapper"
        :class="{ flipped: card.isFlipped }"
        @click="flipCard(card)">

        <Card class="card">
            <div class="card-inner">
                <div class="card-back" v-if="!card.isFlipped">
                    <img src="../assets/cards/faceDown.jpg" alt="Card Back" class="card-img" />
                </div>

                <div class="card-content" v-else>
                    <img :src="card.image" alt="Playing Card" class="card-img" />
                </div>
            </div>
        </Card>
      </div>
   </div>
</template>
  
  <script>
  import Card from "primevue/card";
  
  export default {
    components: { Card },
    data() {
      return {
        cards: [
            { id: 1, image: require("@/assets/cards/aceHearts.webp"), isFlipped: false },
            { id: 2, image: require("@/assets/cards/twoHearts.png"), isFlipped: false },
            { id: 3, image: require("@/assets/cards/threeClubs.png"), isFlipped: false },
            { id: 4, image: require("@/assets/cards/fourDiamonds.png"), isFlipped: false },
            { id: 5, image: require("@/assets/cards/fiveSpaces.jpg"), isFlipped: false },
            { id: 6, image: require("@/assets/cards/sixDiamonds.png"), isFlipped: false },
            { id: 7, image: require("@/assets/cards/sevenClubs.webp"), isFlipped: false },
            { id: 8, image: require("@/assets/cards/eightSpades.png"), isFlipped: false },
        ],
      };
    },
    methods: {
      flipCard(card) {
        card.isFlipped = !card.isFlipped;
      },
    },
  };
  </script>
  
  <style scoped>
  .card-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
  padding: 20px;
}

.card-wrapper {
  perspective: 1000px;
  cursor: pointer;
  width: 100px;
  height: 140px;
}

.card {
  width: 100px;
  height: 140px;
  transform-style: preserve-3d;
  transition: transform 0.5s;
  display: flex;
  align-items: center;
  justify-content: center;
}

.card-inner {
  width: 100px;
  height: 140px;
  display: flex;
  align-items: center;
  justify-content: center;
  backface-visibility: hidden;
}

.card-wrapper.flipped .card {
  transform: rotateY(180deg);
}

.card-content {
  display: flex;
  align-items: center;
  justify-content: center;
}

.card-back {
  transform: rotateY(180deg);
}

.card-img {
  width: 80px;
}
</style>