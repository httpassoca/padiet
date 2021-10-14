<template>
  <main class="text-gray-700 dark:text-gray-200">
    <nav>
      <router-link to="items">
        Items
      </router-link>
      <router-link to="meals">
        Meals
      </router-link>
    </nav>
    <router-view />
    <Footer />
  </main>
</template>

<style lang="sass" scoped>
nav
  display: flex
  flex-direction: column
  padding: 15px

  a
    color: #ccc
    font-size: 1.5rem
</style>
