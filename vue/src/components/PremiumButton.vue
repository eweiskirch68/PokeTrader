<template>
    <div>
        <!--*<p>Standard users can have up to 100 unique cards in their collection.</p> -->
        <button @click="redirectToPremium" id="go-premium">Go Premium!</button>
    </div>
</template>

<script>
export default {
    name: 'premium-button',
    methods: {
        redirectToPremium() {
            this.$store.commit('TOGGLE_SEARCHING_OFF');
            this.$router.push({ name: "premium" });
        },
    }
}
</script>

<style>
button {
  background-color: #3466af;
  color: white;
  border: none;
  border-radius: 5px;
  font-family: "Pokemon Solid", sans-serif;
  text-align: center;
  line-height: 1.5em;
  text-justify: auto;
  letter-spacing: 1px;
  padding-bottom: 5px;
  display: inline-block;
  cursor: pointer;
  width: 100px;
  height: 90px;
  align-self: center;
}
</style>