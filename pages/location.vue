<template>
  <v-layout row>
    <v-flex
      xs12
      sm6
      offset-sm3
    >
      <v-card>
        <v-list three-line>
          <template v-for="(item, index) in items">
            <v-subheader
              v-if="item.header"
              :key="item.header"
            >
              {{ item.header }}
            </v-subheader>

            <v-divider
              v-else-if="item.divider"
              :key="index"
              :inset="item.inset"
            ></v-divider>

            <v-list-tile
              v-else
              :key="item.title"
              avatar
              @click=""
            >
              <v-list-tile-content>
                <v-list-tile-title v-html="item.title"></v-list-tile-title>
                <v-list-tile-sub-title v-html="item.subtitle"></v-list-tile-sub-title>
              </v-list-tile-content>
            </v-list-tile>
          </template>
        </v-list>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { header: "據點" },
        { divider: true, inset: true },
        {
          title: "苗栗",
          subtitle: "苗栗縣頭屋鄉明德村明德路158之12號一樓"
        },
        { divider: true, inset: true },
        {
          title: "高雄",
          subtitle: "高雄市森園區普願寺"
        },
        { divider: true, inset: true }
      ]
    };
  }
};
</script>

<style>
</style>
