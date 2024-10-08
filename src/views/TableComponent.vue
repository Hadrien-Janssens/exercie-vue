<template>
  <h1>Mon super tableau</h1>

  <table class="border w-full">
    <tr>
      <th class="border" @click="sort('nom')">nom</th>
      <th class="border" @click="sort('prenom')">prenom</th>
      <th class="border" @click="sort('role')">role</th>
    </tr>
    <tr class="hover:bg-gray-200" v-for="(user, index) in users" :key="index">
      <td
        class="border p-2 text-center"
        :class="{ 'bg-slate-100': index % 2 == 0 }"
      >
        {{ user.nom }}
      </td>
      <td
        class="border p-2 text-center"
        :class="{ 'bg-slate-100': index % 2 === 0 }"
      >
        {{ user.prenom }}
      </td>
      <td
        class="border p-2 text-center"
        :class="{ 'bg-slate-100': index % 2 === 0 }"
      >
        {{ user.role }}
      </td>
    </tr>
  </table>
</template>

<script setup lang="ts">
import { ref } from "vue";

const users = ref([
  {
    nom: "Durand",
    prenom: "Alice",
    role: "admin",
  },
  {
    nom: "Lemoine",
    prenom: "Bruno",
    role: "user",
  },
  {
    nom: "Martin",
    prenom: "Caroline",
    role: "admin",
  },
  {
    nom: "Dupont",
    prenom: "David",
    role: "user",
  },
  {
    nom: "Lambert",
    prenom: "Elodie",
    role: "user",
  },
  {
    nom: "Rousseau",
    prenom: "François",
    role: "admin",
  },
  {
    nom: "Moreau",
    prenom: "Gabrielle",
    role: "user",
  },
  {
    nom: "Leclerc",
    prenom: "Hugo",
    role: "user",
  },
  {
    nom: "Vidal",
    prenom: "Isabelle",
    role: "admin",
  },
  {
    nom: "Blanc",
    prenom: "Jacques",
    role: "user",
  },
]);
const tri = ref<string | null>(null);

const sort = (champ: string) => {
  if (tri.value === null || tri.value === "desc") {
    users.value.sort((a, b) => {
      return a[champ].localeCompare(b[champ], "fr", {
        ignorePunctuation: true,
      });
    });
    tri.value = "asc";
  } else {
    users.value.sort((a, b) => {
      return b[champ].localeCompare(a[champ], "fr", {
        ignorePunctuation: true,
      });
    });
    tri.value = "desc";
  }
};
</script>
