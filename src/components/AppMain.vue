<script>
// import axios
import axios from 'axios';

export default {
    data() {
        return { 
          message: 'Yu-Gi-Oh Api',
          characters: []
        }
    },
  created() {
    axios
        .get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
        .then((res) => {
            console.log('oggetto creato da axios',res);
            console.log('dati che ci ha risposto il server', res.data);

            // salva dati
            this.characters = res.data.data;
        });
  }
}
</script>

<template>
    <main>
        <!-- select section -->
        <section class="select-section">
            <select name="" id="">
                <option value="">Alien</option>
                <option value="">   </option>
                <option value=""></option>
            </select>
        </section>

        <!-- cards section -->
        <section class="cards-section bg-white">
            <!-- founded content -->
            <div class="founder-main">
                <p>
                    <b>
                        founded ? cards
                    </b>
                </p>
            </div>

            <!-- cards box -->
             <div class="cards-box">
                <!-- card -->
                 <div v-for="(character, i) in characters" :key="i" class="card">
                     <img :src="[character.card_images].image_url" :alt="character.name">
                     <h6>{{ character.name }}</h6>
                     <p>{{ character.archetype }}</p>
                 </div>
             </div>
        </section>
    </main>
</template>

<style lang="scss">
@use '../assets/scss/main.scss' as*;
</style>
