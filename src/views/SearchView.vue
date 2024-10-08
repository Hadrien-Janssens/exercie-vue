<template>
  <div class="flex justify-start items-center gap-5 my-2">
    <p class="">Nombre de proposition :</p>
    <Input type="number" v-model="limit" class="basis-0 grow w-6" />
  </div>
  <Input
    placeholder="Choose your favorite country"
    v-model="search"
    @input="filterArray"
    @focus="
      () => {
        isFocus = true;
        isSelected = false;
      }
    "
  />

  <Card class="mt-2" v-if="isFocus && !isSelected">
    <p
      v-for="(country, index) in filterArray()"
      :key="index"
      @click="select(country)"
    >
      {{ country }}
    </p>
  </Card>
</template>

<script setup lang="ts">
import Card from "@/components/ui/card/Card.vue";
import Input from "@/components/ui/input/Input.vue";
import { ref } from "vue";

const countries = ref([
  "Afghanistan",
  "Albania",
  "Argentina",
  "Australia",
  "Austria",
  "Belgium",
  "Brazil",
  "Canada",
  "China",
  "Colombia",
  "Denmark",
  "Egypt",
  "Finland",
  "France",
  "Germany",
  "Greece",
  "India",
  "Indonesia",
  "Italy",
  "Japan",
  "Kenya",
  "Mexico",
  "Netherlands",
  "New Zealand",
  "Norway",
  "Pakistan",
  "Portugal",
  "South Africa",
  "Spain",
  "United States",
]);
const isFocus = ref(false);
const search = ref("");
const limit = ref(5);
const isSelected = ref(false);

const select = (country: string) => {
  search.value = country;
  isSelected.value = false;
  isFocus.value = false;
};

const filterArray = (): Array<string> => {
  if (search.value === "") {
    return limitTo(countries.value, limit.value);
  } else {
    const filteredArray = countries.value.filter((country) => {
      return country.toLowerCase().includes(search.value.toLowerCase());
    });

    if (filteredArray.length === 0) {
      return ["Pas de donnée disponible"];
    }

    return limitTo(filteredArray, limit.value);
  }
};

const limitTo = (countries: Array<string>, limit = 10): Array<string> => {
  const limitedArray = [];
  for (let index = 0; index < limit; index++) {
    limitedArray.push(countries[index]);
  }

  return limitedArray;
};
</script>
