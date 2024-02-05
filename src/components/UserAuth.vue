<template>
  <button v-if="!userIsAuthenticated" @click="login">
    Login
  </button>
  <button v-else @click="logout" >Logout</button>
</template>

<script>
import { mapActions } from 'vuex';
import { mapGetters } from 'vuex';

export default {
    methods: {
        ...mapActions(['login','logout'])
    },
    computed:{
    ...mapGetters(['userIsAuthenticated'])
  }
  
};
</script>
