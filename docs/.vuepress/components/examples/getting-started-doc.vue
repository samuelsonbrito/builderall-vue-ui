<template>
  <div>
    <bui-sidebar
      :menus="menus"
      :menus-bottom="menus"
      :sidebar-state="sidebarState"
    />

    <bui-navbar
      @toggle-sidebar="toggleSidebar"
      :sidebar-state="sidebarState"
      logo="https://booking.builderall.com/images/images/meta/logo.png"
    />

    <bui-container :sidebar-state="sidebarState">
      <bui-page
        title="Dashboard"
        subtitle="Welcome to a Builderall application!"
      >
        <template #page-header-right>
          <b-button variant="primary" class="ml-auto">
            <bui-icon name="plus" white :size="18"></bui-icon>
            New calendar
          </b-button>
        </template>
        <bui-alert index="alert-01" content="Welcome!" />
      </bui-page>
    </bui-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      sidebarState: "expanded",
      menus: [{ title: "Item", icon: "gear", href: "#" }],
    };
  },
  methods: {
    toggleSidebar(state) {
      this.sidebarState = state;
    },
  },
};
</script>