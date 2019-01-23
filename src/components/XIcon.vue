<template>
  <div :class="cssClass" @click="hdlClick">
    <icon-base :width="size" :height="size" :iconName="icon" :style="{color: cmpColor, fontSize:size+'px'}" >
      <component :is="icon"/>
    </icon-base>
    <div class="bubble-spinner" :style="{width: size+'px', height:size+'px', marginLeft: '-'+size/2+'px'}"></div>
  </div>
</template>

<script>
import IconBase from "./IconBase.vue";
//Icons
import CheckAll from "./icons/CheckAll.vue";
import CheckboxBlankOutline from "./icons/CheckboxBlankOutline.vue";
import CheckboxMarked from "./icons/CheckboxMarked.vue";
import FileUpload from "./icons/FileUpload.vue";
import TimeLapse from "./icons/TimeLapse.vue";
import Settings from "./icons/Settings.vue";
import Edit from "./icons/Edit.vue";
import BookMark from "./icons/BookMark.vue";
import ArrowDropDown from "./icons/ArrowDropDown.vue";
import Folder from "./icons/Folder.vue";
import AddShoppingCart from "./icons/AddShoppingCart.vue";
import Menu from "./icons/Menu.vue";
import ZoomInOutline from "./icons/ZoomInOutline.vue";
import ZoomOutOutline from "./icons/ZoomOutOutline.vue";
import Grid from "./icons/Grid.vue";
import Bug from "./icons/Bug.vue";
import ChevronDown from "./icons/ChevronDown.vue";
import KeyboardReturn from "./icons/KeyboardReturn.vue";
import ContentSave from "./icons/ContentSave.vue";
import NewReleases from "./icons/NewReleases.vue";
import TruckDelivery from "./icons/TruckDelivery.vue";
import ArrowDown from "./icons/ArrowDown.vue";
import ArrowUp from "./icons/ArrowUp.vue";
import PaperClip from "./icons/PaperClip.vue";
import MessageReplyText from "./icons/MessageReplyText.vue";
import ArrowLeft from "./icons/ArrowLeft.vue";
import ArrowRight from "./icons/ArrowRight.vue";
import Launch from "./icons/Launch.vue";
import ChevronLeft from "./icons/ChevronLeft.vue";
import ChevronRight from "./icons/ChevronRight.vue";
import Plus from "./icons/Plus.vue";
import FilterVariant from "./icons/FilterVariant.vue";
import Send from "./icons/Send.vue";
import Close from "./icons/Close.vue";
import Forward from "./icons/Forward.vue";
import Pause from "./icons/Pause.vue";
import Undo from "./icons/Undo.vue";
import ClipboardAlert from "./icons/ClipboardAlert.vue";
import Exclamation from "./icons/Exclamation.vue";
import AccountMultiple from "./icons/AccountMultiple.vue";
import History from "./icons/History.vue";
import Magnify from "./icons/Magnify.vue";
import Calendar from "./icons/Calendar.vue";
import Inbox from "./icons/Inbox.vue";
import Account from "./icons/Account.vue";
import FileDocumentBoxMultiple from "./icons/FileDocumentBoxMultiple.vue";
import BellOutline from "./icons/BellOutline.vue";
import CommentOutline from "./icons/CommentOutline.vue";
import Domain from "./icons/Domain.vue";
import SortVariant from "./icons/SortVariant.vue";
import ViewHeadline from "./icons/ViewHeadline.vue";
import ViewColumn from "./icons/ViewColumn.vue";
import Refresh from "./icons/Refresh.vue";
import SubdirectoryArrowLeft from "./icons/SubdirectoryArrowLeft.vue";
import RadioboxBlank from "./icons/RadioboxBlank.vue";
import RadioboxMarked from "./icons/RadioboxMarked.vue";
import SettingsBox from "./icons/SettingsBox.vue";
import ViewList from "./icons/ViewList.vue";

export default {
  components: {
    IconBase,
    CheckAll,
    CheckboxBlankOutline,
    CheckboxMarked,
    FileUpload,
    TimeLapse,
    Settings,
    Edit,
    BookMark,
    ArrowDropDown,
    Folder,
    AddShoppingCart,
    Menu,
    ZoomInOutline,
    ZoomOutOutline,
    Grid,
    Bug,
    ChevronDown,
    KeyboardReturn,
    ContentSave,
    NewReleases,
    TruckDelivery,
    ArrowDown,
    ArrowUp,
    PaperClip,
    MessageReplyText,
    ArrowLeft,
    ArrowRight,
    Launch,
    ChevronLeft,
    ChevronRight,
    Plus,
    FilterVariant,
    Send,
    Close,
    Forward,
    Pause,
    Undo,
    ClipboardAlert,
    Exclamation,
    AccountMultiple,
    History,
    Magnify,
    Calendar,
    Inbox,
    Account,
    FileDocumentBoxMultiple,
    BellOutline,
    CommentOutline,
    Domain,
    SortVariant,
    ViewHeadline,
    ViewColumn,
    Refresh,
    SubdirectoryArrowLeft,
    RadioboxBlank,
    RadioboxMarked,
    SettingsBox,
    ViewList
  },
  props: ["icon", "size", "color", "spin"],
  data() {
    return { animateClick: true, clicked: false };
  },
  computed: {
    cssClass() {
      let res = ["host", "xicon", "x-icon"];
      if (this.spin) {
        res.push("spin");
      }
      if (this.clicked) {
        res.push("clicked");
      }
      // if (this.size == 36) {
      //   res.push("bubble-spinner-36");
      // } else if (this.size == 48) {
      //   res.push("bubble-spinner-48");
      // }
      if (this.animateClick) {
        res.push("animate-click");
      }
      return res;
    },
    cmpColor() {
      return this.color == "default" ? "" : this.color;
    }
  },
  methods: {
    hdlClick() {
      // this.$xf().log("hdlClick");
      if (this.animateClick) {
        this.clicked = true;
        setTimeout(() => (this.clicked = false), 750);
      }
    }
  }
};
</script>

<style scoped>
.selected .x-icon,
.x-primary .x-icon,
.primary .x-icon {
  color: var(--x-primary);
}
.host {
  position: relative;
}
.bubble-spinner {
  display: none;
  position: absolute;
  top: 0px;
  /*left: -4px;*/
  /* width: 33px;
  height: 33px; */
  /* margin: 100px auto; */
  left: 50%;
  /* margin-left: -20px; */
  background-color: #333;
  border-radius: 100%;
  -webkit-animation: sk-scaleout 1s infinite ease-in-out;
  animation: sk-scaleout 1s infinite ease-in-out;
}
.bubble-spinner-48 .bubble-spinner {
  top: -4px;
  left: -2px;
  width: 60px;
  height: 60px;
}
.bubble-spinner-36 .bubble-spinner {
  width: 65px;
  height: 65px;
  top: -14px;
  left: -7px;
}
.clicked.animate-click .bubble-spinner {
  -webkit-animation: sk-scaleout 0.3s 1 ease-in-out forwards;
  animation: sk-scaleout 0.3s 1 ease-in-out forwards;
}

.spin .bubble-spinner,
.clicked .bubble-spinner {
  display: block;
}

@-webkit-keyframes sk-scaleout {
  0% {
    -webkit-transform: scale(0);
  }
  100% {
    -webkit-transform: scale(1);
    opacity: 0;
  }
}

@keyframes sk-scaleout {
  0% {
    -webkit-transform: scale(0);
    transform: scale(0);
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 0;
  }
}
</style>
