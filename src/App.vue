<template>
  <nav>
    <router-link to="/items">Items</router-link>
    <router-link to="/refeições">Refeições</router-link>
    <router-link to="/metas">Metas</router-link>
    <router-link to="/logout">Logout</router-link>
  </nav>
  <div class="page">
    <router-view/>
  </div>
  <Diet class="diet"/>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Diet from '@/components/Diet.vue';

@Options({
  components: { Diet },
})

export default class App extends Vue {}
</script>

<style lang="sass">
*
  padding: 0
  margin: 0
  outline: none
  box-sizing: border-box

#app
  display: flex
  font-family: Avenir, Helvetica, Arial, sans-serif
  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  color: #2c3e50

nav
  height: 100vh
  width: 250px
  display: flex
  flex-direction: column
  padding: 20px
  background-color: #191919
  a
    font-weight: bold
    color: #ccc

    &.router-link-exact-active
      color: #42b983
.page
  background-color: red
  flex-grow: 1
.diet
  background-color: #191919
  width: fit-content
  flex-grow: 1
</style>
