<template>
  <v-card v-ripple class="mx-auto" max-width="500" outlined>
    <v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title class="headline mb-1">{{ title }}</v-list-item-title>
        <v-list-item-subtitle class="title">
          {{
          subtitle
        }}</v-list-item-subtitle>

      </v-list-item-content>
              <img :src="avatar_ic" width="60px" height="60px" alt="">

    </v-list-item>
  </v-card>
</template>

<script>
export default {
  name: "StockCard",
  mounted() {
    this.getIcon();
  },
  props: ["title", "subtitle", "avatar_bg", "avatar_ic"],
  data() {
    return {
      icon_data: {
        icon_wait: "mdi-account-clock",
        icon_con: "mdi-comment-account",
        icon_inter: "mdi-account-question",
        icon_hiring:"mdi-account-check-outline",
        icon_fail:"mdi-account-remove-outline"
      },
      icon_set_up: ""
    };
  },
  methods: {
    getIcon(){
          if(this.title == "Waitting"){
            this.icon_set_up = this.icon_data.icon_wait
          }else if (this.title == "HR Consider"){
            this.icon_set_up = this.icon_data.icon_con
          }else if (this.title == "Interview"){
            this.icon_set_up = this.icon_data.icon_inter
          }else if (this.title == "Hiring"){
            this.icon_set_up = this.icon_data.icon_hiring
          }else if (this.title == "Fail"){
            this.icon_set_up = this.icon_data.fail
          }
    },
  },
};
</script>

<style></style>
