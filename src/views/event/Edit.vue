<template>
  <div v-if="event">
    <h1>{{ event.tittle }}</h1>
    <div id="nav">
      <router-link :to="{ name: 'EventDetails', params: { id } }">
        Details
      </router-link>
      |
      <router-link :to="{ name: 'EventRegister', params: { id } }">
        Register
      </router-link>
      |
      <router-link :to="{ name: 'EventEdit', params: { id } }">
        Edit
      </router-link>
    </div>
    <p>Edit the event here</p>
  </div>
</template>