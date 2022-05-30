<template>
  <div>
    <p class="bg-green-900 text-white">
      {{ authors.data.authors.data[0].attributes.name }}
    </p>
    <NuxtWelcome />
  </div>
</template>
<script setup lang="ts">
import { authorQuery } from '~/graphql/query'
const graphql = useStrapiGraphQL()

const authors = await graphql(authorQuery)
</script>
