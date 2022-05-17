<template>
  <v-app>
    <v-app-bar theme="dark"> </v-app-bar>

    <v-navigation-drawer theme="dark" rail permanent>
      <v-list-item
        prepend-avatar="https://randomuser.me/api/portraits/men/75.jpg"
      ></v-list-item>

      <!-- <v-divider></v-divider> -->

      <v-list density="compact" nav>
        <v-list-item
          prepend-icon="mdi-view-dashboard"
          value="dashboard"
        ></v-list-item>
        <v-list-item prepend-icon="mdi-forum" value="messages"></v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-navigation-drawer permanent theme="dark">
      <v-card class="ma-4 elevation-10 rounded-20" height="90vh">
        <v-list>
          <v-list-item
            title="Главная"
            value="home"
            to="/"
            active-color="blue"
          ></v-list-item>
          <v-list-item
            title="Пользователи"
            value="users"
            to="/users"
            active-color="blue"
          ></v-list-item>
          <v-list-item
            title="Информация"
            value="about"
            to="about"
            active-color="blue"
          ></v-list-item>
          <v-list-item
            title="Контакты"
            value="contacts"
            to="/contacts"
            active-color="blue"
          ></v-list-item>
          <v-list-item
            title="Настройки"
            value="settings"
            to="/settings"
            active-color="blue"
          ></v-list-item>
        </v-list>
      </v-card>
    </v-navigation-drawer>

    <v-main>
      <v-card id="main_card" theme="dark" class="ma-4 elevation-4" height="90vh">
        <router-view />
      </v-card>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    //
  }),
};
</script>

<style scoped>
boby {
  margin: 0 auto;
  display: flex;
  justify-content: center;
  text-decoration: none;
}

#main-card {
  margin: 40px;
  margin-bottom: 100px;
}

router-link {
  text-decoration: none;
}
</style>
