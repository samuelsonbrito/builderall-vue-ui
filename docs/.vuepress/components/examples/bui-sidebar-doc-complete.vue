<template>
  <div>
    <bui-sidebar
      :sidebar-state="state"
      active-menu="sites"
      :user="user"
      :menus="menus"
      :menus-bottom="menus_bottom"
      :menus-mobile="menus_mobile"
    >
    </bui-sidebar>

    <div class="my-3">
      <b-button class="mx-1" v-b-toggle.sidebar-mobile>mobile</b-button>
      <b-button class="mx-1" @click="state = 'mini'">mini</b-button>
      <b-button class="mx-1" @click="state = 'expanded'">expanded</b-button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      state: "expanded",
      user: {
        name: "Mauricio Testa",
        email: "mauriciotesta@gmail.com",
        locale: "pt_BR",
        gravatar:
          "https://secure.gravatar.com/avatar/2253502b4562dad48c2c74681c459dd1",
      },
      menus: [
        {
          title: "Dashboard",
          routes: ["dashboard"],
          icon: "dashboard",
          href: "/",
        },
        {
          title: "Sites",
          routes: ["sites"],
          name: "config",
          icon: "gear",
          href: "/",
        },
      ],
      menus_bottom: [{ title: "Office", icon: "logo", href: "#" }],
      menus_mobile: [{ title: "Mobile!", icon: "lang", href: "#" }],
    };
  },
};
</script>