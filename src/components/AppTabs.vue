<template>
  <div class="tabs">
   <ul class="tab-links">
     <li v-for="tab in tabs" :class="{'active':tab.active}" @click="set Active(tab)">{{tab.label}}</li>
   </ul>
   <slot></slot>

   
  </div>
</template>

<script>
export default {
  name: 'AppTabs',
  data: function() {
    return{
      tabs:[]
    };
  },
  created: function() {
    this.tabs = this.$children;
  },
  methods: {
    setActive: function(tab) {
    this.tabs.forEach(function (t) {
      t.active = t === tab;
    });
   }
  }

}
</script>

<style scoped>
  .app-tabs {
  background: rgb(114, 113, 113);
  }
</style>
