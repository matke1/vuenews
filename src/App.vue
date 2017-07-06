<template>
  <div id="app" class="container">
    <SourceSelection v-bind:sourceChanged="sourceChanged" ></SourceSelection>
    <Newslist v-bind:source="source" ></Newslist>
  </div>
</template>

<script>
  import SourceSelection from './components/SourceSelection.vue'
  import NewsList from './components/NewsList.vue'


export default {
  name: 'app',
  components: {
    SourceSelection,
    NewsList
  },
  data(){
      return{
          source: ''
      }
  },
  methods:{
      sourceChanged: function (source) {
        this.source = source;
      }
  }
}
</script>

<style>
#app {
  padding-top: 20px;
}
</style>
