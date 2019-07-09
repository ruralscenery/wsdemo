<template>

    <section>
      <header>
        <h1>會員: {{member.name}}</h1>
      </header>

      <v-list two-line>
        <v-list-tile v-for="(point, index) in points" :key="index">
          <v-list-tile-content>
            <v-list-tile-title>{{point.title}}</v-list-tile-title>
            <v-list-tile-sub-title>{{point.value}}</v-list-tile-sub-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </section>

</template>

<script>
export default {
  data() {
    return {
      member: {
        name: "我的名字"
      },
      points: [{"title": "上月剩餘點數", "value": 1000},
      {"title": "本月加值點數", "value": 1000},
      {"title": "下月預扣點數", "value": 1000}
      ]
    };
  }
};
</script>
