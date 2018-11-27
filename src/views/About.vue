<template>
  <section class="about">
    <v-tabs 
      left
      hide-slider
      class="mainTabs"
    >
      <v-tab :ripple="false" class="mainTab">
        Nam mi kyung (ux planner)
      </v-tab>
      <v-tab :ripple="false" class="mainTab">
        Yu eun hye (designer)
      </v-tab>
      <v-tab :ripple="false">
        Kim yu mi (publisher)
      </v-tab>
      <v-tab-item>
        <v-layout row wrap>
        <v-flex xs12 sm4>
          <ul class="">
            <li v-for="(item, i) in portfolio" :key="i" @click="handleDetail(i)">{{item.title}}</li>
          </ul>
        </v-flex>
        <v-flex xs12 sm8>
          <div class="detail">
            <p>work: {{correntTitle}}</p>
            <p>client: {{correntClient}}</p>
            <div class="imgWrap">
              <img :src="require(`@/assets/images/${currentPath}`)">
            </div>
          </div>
        </v-flex>
        </v-layout>
      </v-tab-item>
      <v-tab-item>
        123
      </v-tab-item>
      <v-tab-item>
        123
      </v-tab-item>
    </v-tabs>
  </section>
</template>

<script>
export default {
  name: 'about',
  components: {},
  data () {
    return {
      correntTitle: '우리은행 위비톡 PC application 1.0',
      correntClient: '우리은행',
      currentPath: 'sample.png',
      portfolio: [{
        title: '우리은행 위비톡 PC application 1.0',
        client: '우리은행',
        url: 'sample'
      }, {
        title: '고영테크놀러지 OCT 의료 장비',
        client: '우리은행2',
        url: 'sample'
      }, {
        title: '고영테크놀러지 AOI 장비',
        client: '우리은행2',
        url: 'sample'
      }, {
        title: 'SK Broadband 옥수수 Mobile',
        client: '우리은행2',
        url: '/'
      }, {
        title: '라이프스타일 쇼핑몰 Urbanchild',
        client: '우리은행2',
        url: '/'
      }, {
        title: 'Video editing app 롤리캠',
        client: '우리은행2',
        url: '/'
      }, {
        title: '자동차 소셜네트워크 CARnect',
        client: '우리은행2',
        url: '/'
      }]
    }
  },
  methods: {
    handleDetail(i) {
      this.correntTitle = this.portfolio[i].title
      this.correntClient = this.portfolio[i].client
      this.currentPath = this.portfolio[i].url
    }
  }
}
</script>