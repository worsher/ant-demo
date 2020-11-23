<template>
  <a-menu
  theme="dark"
  mode="inline"
  v-model:selectedKeys="selectedKeys">
    <a-menu-item key="1">
      <component :is="a"></component>
      <user-outlined />
      <span>nav 1</span>
    </a-menu-item>

    <a-menu-item key="2">
      <user-outlined />
      <span>nav 2</span>
    </a-menu-item>

    <a-menu-item key="3">
      <user-outlined />
      <span>nav 3</span>
    </a-menu-item>
  </a-menu>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { UserOutlined } from '@ant-design/icons-vue'

export default defineComponent({
  components: {
    UserOutlined
  },
  data () {
    return {
      selectedKeys: ['1'],
      a: UserOutlined
    }
  }
})
</script>
