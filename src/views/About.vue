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
        <ul>
          <li v-for="(item, i) in portfolio" :key="i">{{item.title}}</li>
        </ul>
        <Detail/>
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
      portfolio: [{
        title: '우리은행 위비톡 PC application 1.0',
        client: '우리은행',
        url: '/'
      }, {
        title: '우리은행 위비톡 PC application 1.0',
        client: '우리은행',
        url: '/'
      }]
    }
  }
}
</script>