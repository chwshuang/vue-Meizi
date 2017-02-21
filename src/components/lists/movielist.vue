<template>
  <div class="list" v-infinite-scroll="loadMore" infinite-scroll-disabled="busy" infinite-scroll-distance="100">
      <a v-for="data in datas" :href="data.url " target="view_window">
         <v-card :data="data" ></v-card>
      </a>
  </div>

</template>

<script type="text/ecmascript-6">
  import vCard from '../moviecard/card.vue';
  export default
  {
    name: 'v-list',
    props: {
      type: {
        type: String
      }
    },
    data() {
      return {
        datas: [],
        page: 1,
        busy: false
      };
    },
    computed: {

    },
    methods: {
      loadTop() {
        this.$store.commit('UPDATE_LOADING', true);
        this.$http.get(`http://localhost:8080/api/data/movie/${this.page}`).then((response) => {
          this.datas = this.datas.concat(response.body.data);
          this.busy = false;
          this.$nextTick(() => {
          this.$store.commit('UPDATE_LOADING', false);
          });
        });

//        this.datas = this.datas.concat([{name: '刺客信条', desc: '穿越黑科技，法鲨炫腹肌', country: '美国', scope: '7.9', date: '2017-12-10', type: '喜剧,动作,儿童', src: '//p0.meituan.net/165.220/movie/e631df85c6cadddafc6792cd94fd14ad6081426.jpeg.webp'}, {name: '爱乐之城', desc: '爵士钢琴家，恋爱舞天涯', country: '美国', date: '2017-12-10', type: '喜剧,动作,儿童', scope: '7.8', src: '//p0.meituan.net/165.220/movie/968965a2dde3d27a192b6e6881fff9d8119572.jpeg.webp'}]);
//          this.busy = false;
//          this.$nextTick(() => {
//          this.$store.commit('UPDATE_LOADING', false);
//          });
      },
      loadMore() {
        this.busy = true;
        this.loadTop();
        this.page++;
      }
    },
    components: {
      vCard
    }
  };
</script>
<style lang="stylus" rel="stylesheet/stylus">
  .list {
    padding: 0px;
  }
</style>
