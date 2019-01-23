<template>
  <div id="app">
    <div class="wrapper">
    <button>
      <XIcon size="35"  icon="check-all" color="darkorchid" :spin="true"></XIcon>
    </button>
    <button>
      <XIcon size="20"  icon="checkbox-blank-outline" color="red" :spin="false"></XIcon>
    </button>
      <XIcon size="20"  icon="checkbox-marked" color="blue"></XIcon>
      <XIcon size="36"  icon="file-upload" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="time-lapse" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="settings" color="darkorchid"></XIcon>
      <XIcon size="16"  icon="edit" color="darkorchid"></XIcon>
      <XIcon size="16"  icon="book-mark" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="arrow-drop-down" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="folder" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="add-shopping-cart" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="Menu" color="darkorchid"></XIcon>
      <XIcon size="25"  icon="zoom-in-outline" color="darkorchid"></XIcon>
      <XIcon size="25"  icon="zoom-out-outline" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="grid" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="bug" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="chevron-down" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="keyboard-return" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="content-save" color="darkorchid"></XIcon>
      <XIcon size="36"  icon="arrow-down" color="darkorchid"></XIcon>
      <XIcon size="36"  icon="arrow-up" color="darkorchid"></XIcon>
      <XIcon size="36"  icon="arrow-left" color="darkorchid"></XIcon>
      <XIcon size="36"  icon="arrow-right" color="darkorchid"></XIcon>
    </div>
    <div class="wrapper">
      <XIcon size="30"  icon="paper-clip" color="darkorchid"></XIcon>
      <XIcon size="30"  icon="message-reply-text" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="launch" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="chevron-left" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="chevron-right" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="plus" color="#3fb9d5"></XIcon>
      <XIcon size="24"  icon="filter-variant" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="send" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="close" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="forward" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="pause" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="undo" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="clipboard-alert" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="exclamation" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="account-multiple" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="history" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="magnify" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="calendar" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="inbox" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="account" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="file-document-box-multiple" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="bell-outline" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="comment-outline" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="domain" color="darkorchid"></XIcon>
      <XIcon size="16"  icon="new-releases" color="deeppink"></XIcon>
    </div>

    <div class="wrapper">
      <XIcon size="24"  icon="sort-variant" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="view-headline" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="view-column" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="refresh" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="subdirectory-arrow-left" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="radiobox-blank" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="radiobox-marked" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="settings-box" color="darkorchid"></XIcon>
      <XIcon size="24"  icon="view-list" color="darkorchid"></XIcon>
      <button @click="hdlclick" style="background-color: grey;">Switch icon</button>
      <XIcon v-if="toggle" size="50"  icon="truck-delivery" color="darkorchid"></XIcon>
      <XIcon v-else size="50"  icon="add-shopping-cart" color="darkorchid"></XIcon>
    </div>

      <!-- <icon-heart-face /> -->
  </div>
</template>

<script>
import XIcon from './components/XIcon.vue'

// import IconHeartFace from './components/animatedIcons/IconHeartFace.vue'

export default {
  name: 'app',
  components: {
    XIcon,
  },
  data() {
    return {
     toggle: true
    }
  },
  methods: {
    hdlclick() {
       this.toggle = !this.toggle
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  justify-content: center;
  flex-direction: column;
  flex-wrap: wrap;
}
body{
  --x-primary-bg: rgba(153, 50, 204, 0.02);
  --x-primary-bg-border: rgba(153, 50, 204, 0.045);
  --x-primary-bg1: darkorchid;
  --x-primary: darkorchid;
  --x-primary-rgb: 153, 50, 204;
}
button{
  border: none;
  background: #fff;
  text-align: center;
  outline: none;
}
.wrapper{
  margin-top: 10px;
  display: flex;
  justify-content: center;
  flex-direction: row;
  flex-wrap: wrap;
}
</style>
