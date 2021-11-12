<template>
  <b-container class="b-container">
    <b-row class="my-5">
      <b-col lg="8">
        <h3>Company Inc.</h3>
      </b-col>
      <b-col>
        <NuxtLink to="/">Home</NuxtLink>
        <NuxtLink to="pricing" class="ml-4">Pricing</NuxtLink>
      </b-col>
    </b-row>
    <b-row>
      <b-col>
        <Nuxt />
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: 'Default',
};
</script>

<style lang="scss" scoped>

</style>
