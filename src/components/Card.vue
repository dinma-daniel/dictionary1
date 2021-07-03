<template>
  <div class="container">
    <Search :getSearch="addSearch" />
    <div class="cardd">
      <div class="content" v-for="item in list" :key="item.id">
        <div class="word">
          <div class="audio">
            <i class="fas fa-volume-down fa-2x"></i>
          </div>
          <div class="right">
            <h1 class="name">{{ item.word }}</h1>
            <ul class="pronounce" :v-if="Array.isArray(item.phonetics)">
              <li v-for="(phonetic, idx) in item.phonetics" :key="idx">
                {{ phonetic.text }}
              </li>
            </ul>
          </div>
        </div>
        <div class="contentt">
          <ul :v-if="Array.isArray(item.meanings)">
            <li v-for="(meaning, idx) in item.meanings" :key="idx">
              <span :v-if="meaning?.partOfSpeech">{{
                meaning.partOfSpeech
              }}</span>
              <ul :v-if="meaning?.definitions">
                <li v-for="(definition, idx) in meaning.definitions" :key="idx">
                  <span>defination: {{ definition.definition }}</span>
                  <span>example: {{ definition.example }}</span>
                </li>
              </ul>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Search from '../components/Search.vue'
import axios from 'axios'

export default {
  name: 'Card',
  props: {},
  components: {
    Search,
  },
  data() {
    return {
      list: null,
      searchh: '',
    }
  },
  computed: {},
  methods: {
    addSearch(search) {
      axios
        .get(`https://api.dictionaryapi.dev/api/v2/entries/en_US/${search}`)
        .then((result) => {
          this.list = result.data
          console.log(result.data)
        })
    },
  },
}
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  /* border: 1px solid red; */

  margin: 0 auto;
}

.cardd {
  /* border: 1px solid red; */
  /* padding: 3rem 0; */
  border-radius: 10px;
  width: 100%;
  background-color: #ffc996;
}

.content {
  /* border: 1px solid black; */
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin: 1rem 3rem;
}

.contentt {
  /* border: 1px solid black; */
  /* margin-top: 4rem; */
  font-weight: 500;
  font-size: 1.5rem;
}

h1 {
  margin: 0;
}

.name {
  font-size: 2rem;
}

.pronounce {
  font-size: 1.3rem;
  font-family: Cormorant;
  font-weight: 500;
}

.word {
  /* border: 1px solid black; */
  display: flex;
}

.audio {
  /* border: 1px solid black;  */
  margin-right: 1.5rem;
}

.fas {
  margin-top: 0.5rem;
}
</style>
