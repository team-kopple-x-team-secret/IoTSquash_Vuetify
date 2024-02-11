<template>
    <v-navigation-drawer 
        class="drawer"
        expand-on-hover
        rail
        v-model="drawer" 
        :rail="rail"
        permanent
        @click="rail = false"
      >
        <v-list-item
        class="avatar"
        prepend-avatar="https://scontent.fmnl3-1.fna.fbcdn.net/v/t39.30808-6/423715315_1437098033867963_1934856792714972248_n.jpg?_nc_cat=108&ccb=1-7&_nc_sid=efb6e6&_nc_eui2=AeH_VGSRYYfCDiWSdBBBabCNLX8-AGc4TrQtfz4AZzhOtEq0lz14C0IT7y0e9cPtkY4KXsfKEZn2BfGZ7Np5oJqg&_nc_ohc=zG6uziamECkAX8BU1Qr&_nc_ht=scontent.fmnl3-1.fna&oh=00_AfBxYN2Vb0QEvSKNemHI8Dfav1bqAl70GJAnTy9iEWPOdQ&oe=65CCBF1E"
        title="Justin Jeremi Cruz"
        nav
        >
          <template v-slot:append>
            <v-btn
              variant="text"
              icon="mdi-chevron-left"
              @click.stop="rail = !rail"
            ></v-btn>
          </template>
        </v-list-item>
        <v-divider></v-divider>
          <v-list class="menu" density="compact" nav>
            <v-list-item class="button" prepend-icon="mdi-gauge" title="Dashboard" value="dashboard"></v-list-item>
            <v-list-item class="button" prepend-icon="mdi-monitor" title="Monitoring" value="monitoring"></v-list-item>
            <v-list-item class="button" prepend-icon="mdi-calendar" title="Data" value="data"></v-list-item>
            <v-list-item class="button" prepend-icon="mdi-information" title="About" value="about"></v-list-item>
          </v-list>
      </v-navigation-drawer>
</template>

<script>
export default {
    data () {
      return {
        drawer: true,
        rail: true,
      }
    },
  }
</script>

<style lang="scss">
  .avatar{
    background-color: var(--grey);
    border-radius: 0%;
    padding-left: 15px;
  }
  .menu{
    &:hover, &.button{
    background-color: var(--dark-alt);
  }
  }
</style>