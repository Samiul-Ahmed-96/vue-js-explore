<template>
  <Binding />
  <Methods />
  <FormHandleAndMore />
  <Article title="Message" :likes="99" :isPublished="true" />
  <hr />
  <h2>Popup Component</h2>
  <hr />
  <button @click="popupShow = true">Show Popup</button>
  <Popup v-show="popupShow" @close="popupShow = false" />
  <Slots><h3>Hello Slot from 1</h3></Slots>
  <Slots><h3>Hello Slot from 2</h3></Slots>
  <Slots
    ><img
      src="https://images.pexels.com/photos/7525204/pexels-photo-7525204.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=200&w=200"
      alt=""
  /></Slots>
  <Slots>
    <template v-slot:header>Its Header</template>
    <template v-slot:default
      ><img
        src="https://images.pexels.com/photos/7525204/pexels-photo-7525204.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=200&w=200"
        alt=""
    /></template>
    <template v-slot:footer>Its footer</template>
  </Slots>

  <hr />
  <h2>Dynamic Components</h2>
  <hr />
  <button @click="activeTab = 'TabA'">Tab A</button>
  <button @click="activeTab = 'TabB'">Tab B</button>
  <button @click="activeTab = 'TabC'">Tab C</button>
  <TabA v-if="activeTab === 'TabA'" />
  <TabB v-if="activeTab === 'TabB'" />
  <TabC v-if="activeTab === 'TabC'" />
  <Request />
  <hr>
  <h2>Template refs load on focus</h2>
  <div class="temRefs">
    <input type="text" ref="inputRefs">
  </div>

  <HoverCounter/>
  <ClickCounter/>
  <hr><h2>Vuex</h2><hr>
  <BookListOne :book="books"></BookListOne>
  <BookListTwo :book="books"></BookListTwo>
</template>

<script>
import Binding from "./components/Binding.vue";
import Methods from "./components/Methods.vue";
import FormHandleAndMore from "./components/FormHandleAndMore.vue";
import Article from "./components/Article.vue";
import Popup from "./components/Popup.vue";
import Slots from "./components/Slots.vue";
import TabA from "./components/TabA.vue";
import TabB from "./components/TabB.vue";
import TabC from "./components/TabC.vue";
import Request from "./components/Request.vue";
import HoverCounter from "./components/HoverCounter.vue";
import ClickCounter from "./components/ClickCounter.vue";
import BookListOne from "./components/BokkListOne.vue";
import BookListTwo from "./components/BookListTwo.vue";
export default {
  name: "App",
  mounted(){
    this.$refs.inputRefs.focus()
  },
  components: {
    Binding,
    Methods,
    FormHandleAndMore,
    Article,
    Popup,
    Slots,
    TabA,
    TabB,
    TabC,
    Request,
    HoverCounter,
    ClickCounter,
    BookListOne,
    BookListTwo


  },

  data() {
    return {
      popupShow: false,
      activeTab: "TabA",
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}
</style>
