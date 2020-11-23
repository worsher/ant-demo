<template>
  <a-layout id="layout">
    <a-layout-sider
    collapsible
    :trigger="null"
    v-model:collapsed="collapsed"
    breakpoint="lg"
    collapsed-width="0"
    @collapse="onCollapse"
    @breakpoint="onBreakpoint">
      <div class="logo">
        admin
      </div>
      <v-menu></v-menu>
    </a-layout-sider>
    <a-layout>
      <a-layout-header style="background-color : #7dbcea">
        <v-header></v-header>
      </a-layout-header>
      <a-layout-content style="background-color : #fff">
        <v-content></v-content>
      </a-layout-content>
      <a-layout-footer>
        <v-footer></v-footer>
      </a-layout-footer>
    </a-layout>
  </a-layout>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import VHeader from './VHeader.vue'
import VMenu from './VMenu.vue'
import VContent from './VContent.vue'
import VFooter from './VFooter.vue'

export default defineComponent({
  components: {
    VHeader,
    VMenu,
    VContent,
    VFooter
  },
  data () {
    return {
      collapsed: false
    }
  },
  setup () {
    console.log('set up')
  }
})
</script>

<style type="text/css">
  #layout{
    height: 100%;
  }
  #layout .logo {
    height: 32px;
    background: rgba(255, 255, 255, 0.2);
    margin: 16px;
    color: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
