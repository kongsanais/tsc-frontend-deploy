<template>
  <v-container>
    <v-row  class="pt-5 pl-5 pr-5" >
      <v-col lg="6" md="6" sm="12" cols="12">
      <v-card>
        <v-card-title>
          <v-icon large left>
            mdi-contacts
          </v-icon>
          <span class="title font-weight-light">Contact / ติดต่อ</span>
        </v-card-title>
        <hr>
        <v-card-text>
          <v-list >
              Ms.Ladda Kaewsringam<br>
              HR/Recruitmen<br>
              Office. 038-320769<br>
              E-mail ladda.k@samsung.com<br>
              Thai Samsung Electronics Co.,Ltd. (Chonburi)
          </v-list>
        </v-card-text>
      </v-card>
      </v-col>
            <v-col lg="6" md="6" sm="12" cols="12">
      <v-card>
        <v-card-title>
          <v-icon large left>
            mdi-contacts
          </v-icon>
          <span class="title font-weight-light">Map / แผนที่</span>
        </v-card-title>
        <hr>
        <v-card-text>
          <v-list >
            <!-- <v-subheader>text</v-subheader> -->
            <v-list-item-group v-model="items" color="primary">
            <section id="section-map" class="clearfix">
              <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d22302.845749770753!2d100.96926935542685!3d13.092923725014074!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0xba8da2649713c6f2!2z4Lia4Lij4Li04Lip4Lix4LiXIOC5hOC4l-C4ouC4i-C4seC4oeC4i-C4uOC4h-C4reC4tOC5gOC4peC5h-C4geC4l-C4o-C4reC4meC4tOC4hOC4quC5jCDguIjguLPguIHguLHguJQ!5e0!3m2!1sth!2sth!4v1569812124378!5m2!1sth!2sth" width="100%" height="400px" frameborder="0" style="border:0" allowfullscreen></iframe>
            </section>
            </v-list-item-group>
          </v-list>
        </v-card-text>
      </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    //  
    items: [
      { text: "Officer/Engineer & Management", icon: "mdi-account-circle-outline" ,link: "/register_engineer" },
      { text: "สมัครงานฝ่ายผลิต", icon: "mdi-account-cog-outline",link: "/register_production" }
    ],
  }),
  methods: {
    onClickMenu(link) {
      this.$router.push(link).catch((err) => {});
    },
  },
};
</script>

<style></style>
