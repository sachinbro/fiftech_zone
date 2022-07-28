<script>
export default{
    props: ['price']
}
</script>
<template>
    <v-btn class="rounded-xl" width="150" color="#E9D1FF" elevation="0">
         {{price ? `Rs.${price}` : 'Contact Us'}}
    </v-btn>
</template>
<style scoped>
    .v-btn {
       text-transform: none !important;
    }
</style>