<template>
  <div class="notification-container">
    <NotificationBar
      v-for="notification in notifications"
      :key="notification.id"
      :notification="notification"
    />
  </div>
</template>

<script>
import NotificationBar from '@/components/NotificationBar.vue'
import { mapState } from 'vuex'

export default {
  components: {
    NotificationBar
  },
  computed: mapState('notification', ['notifications'])
}
</script>

<style scoped>
.notification-container {
  position: fixed;
  top: 0;
  right: 50px;
  padding-right: 40px;
}
</style>