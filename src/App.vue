
<template>
  <div>
    <CountryList>
      <CountryCard v-for="item in list" :key="item.id" :title="item.title" :desc="item.desc" :flag="item.flag" />
    </CountryList>
  </div>
</template>

<script setup>
import CountryCard from '@/components/CountryCard.vue'
import CountryList from '@/components/CountryList.vue'
import { computed, ref } from 'vue'
import { nanoid } from 'nanoid'

const list = ref([
  {
    id: nanoid(),
    flag: 'public/atlas.assets/de.png',
    title: 'Germany',
    desc: 'Federal Republic of Germany is an independent country in Western Europe with an estimated population of over 83 million people.',
    isDependent: false,
    population: '83.000.000',
    continent: 'Europe'

  },
  {
    id: nanoid(),
    flag: '../public/atlas.assets/py.png',
    title: 'Paraguay',
    desc: 'Republic of Paraguay is an independent country in South America with an estimated population of over 7.1 million people.',
    isDependent: false,
    population: '7.100.000',
    continent: 'America'
  },
  {
    id: nanoid(),
    flag: '../public/atlas.assets/ag.png',
    title: 'Antigua and Barbuda',
    desc: 'Antigua and Barbuda is an independent country in Caribbean with an estimated population of over 97 thousand people.',
    isDependent: false,
    population: '97.000',
    continent: 'America'
  },
  {
    id: nanoid(),
    flag: '../public/atlas.assets/in.png',
    title: 'India',
    desc: 'Republic of India is an independent country in Southern Asia with an estimated population of over 1.3 billion people.',
    isDependent: false,
    population: '1.300.000.000',
    continent: 'Asia'
  },
  {
    id: nanoid(),
    flag: '../public/atlas.assets/bf.png',
    title: 'Burkina Faso',
    desc: 'Burkina Faso is an independent country in Western Africa with an estimated population of over 20 million people.',
    isDependent: false,
    population: '20.000.000',
    continent: 'Africa'
  },
  {
    id: nanoid(),
    flag: '../public/atlas.assets/hk.png',
    title: 'Hong Kong',
    desc: "Hong Kong Special Administrative Region of the People's Republic of China is a dependent territory in Eastern Asia  an estimated population of over 7.5 million people.",
    isDependent: true,
    population: '7.500.000',
    continent: 'Asia'
  },
  {
    id: nanoid(),
    flag: '../public/atlas.assets/ae.png',
    title: 'United Arab Emirates',
    desc: 'United Arab Emirates is an independent country in Western Asia with an estimated population of over 9.8 million people.',
    isDependent: false,
    population: '9.800.000',
    continent: 'Asia'
  },
  {
    id: nanoid(),
    flag: '../public/atlas.assets/km.png',
    title: 'Comoros',
    desc: 'Union of the Comoros is an independent country in Eastern Africa with an estimated population of over 8.6 thousand people.',
    isDependent: false,
    population: '8.600',
    continent: 'Africa'
  },
  {
    id: nanoid(),
    flag: '../public/atlas.assets/pn.png',
    title: 'Pitcairn Islands',
    desc: 'Pitcairn Islands is a dependent territory in Polynesia with an estimated population of over 56 people.',
    isDependent: true,
    population: '56',
    continent: 'Oceania'
  },
  {
    id: nanoid(),
    flag: '../public/atlas.assets/bg.png',
    title: 'Bulgaria',
    desc: 'Republic of Bulgaria is an independent country in Southeast Europe with an estimated population of over 6.9 million people.',
    isDependent: false,
    population: '6.900.000',
    continent: 'Europe'
  },
  {
    id: nanoid(),
    flag: '../public/atlas.assets/dj.png',
    title: 'Djibouti',
    desc: 'Republic of Djibouti is an independent country in Eastern Africa with an estimated population of over 9.8 thousand people.',
    isDependent: false,
    population: '9.800',
    continent: 'Africa'
  },
  {
    id: nanoid(),
    flag: '../public/atlas.assets/la.png',
    title: 'Laos',
    desc: "Lao People's Democratic Republic is an independent country in South-Eastern Asia with an estimated population of over 7.2 million people.",
    isDependent: false,
    population: '7.200.000',
    continent: 'Asia'
  },



])

console.log(list.value[0].flag)
</script>

<style scoped></style>
