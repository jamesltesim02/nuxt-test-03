<template>
  <v-layout>
    <v-flex text-xs-center>
      <img
        src="/v.png"
        alt="Vuetify.js"
        class="mb-5"
      >
      <blockquote class="blockquote">
        &#8220;First, solve the problem. Then, write the code.&#8221;
        <footer>
          <small>
            <em>&mdash;{{ userExpand.truename }} </em>
          </small>
        </footer>
      </blockquote>
    </v-flex>
  </v-layout>
</template>
<script>
// import { mapState } from 'vuex'

export default {
  data() {
    console.log('data...') // eslint-disable-line no-console
    return {
      userExpand: {
        truename: this.truename1
      }
    }
  },
  computed: {
    // ...mapState('user', {
    //   username1(state) {
    //     console.log('map state....') // eslint-disable-line no-console
    //     return state.truename1
    //   }
    // })
    username1() {
      console.log('computed....') // eslint-disable-line no-console
      return 'zhangsan'
    }
  },
  created() {
    console.log('created....') // eslint-disable-line no-console
    console.log(this.username1) // eslint-disable-line no-console
  }
}
</script>
