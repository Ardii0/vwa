<template>
  <div>
  </div>
</template>

// <script>
// import Vue from "vue";
// import Component from "vue-class-component";
// import { Prop } from "vue-property-decorator";

// @Component
// export default class LayoutSidebar extends Vue {
//   @Prop({ type: [Boolean], default: false })
//   mobileOpened!: boolean;

//   windowWidth = null as any;

//   sidebarData = [
//     {
//       title: "Dashboard",
//       icon: "speedometer",
//       link: "/",
//     },
//     {
//       title: "In Bound",
//       icon: "package-down",
//       link: "/in-bounds",
//     },
//     {
//       title: "Out Bound",
//       icon: "package-up",
//       link: "/out-bounds",
//     },
//     {
//       title: "Seller",
//       icon: "account-supervisor-circle",
//       link: "/sellers",
//     },
//   ];

//   sidebarAdminData = [
//     {
//       title: "User Management",
//       icon: "account",
//       link: "/user-management",
//     },
//     {
//       title: "Warehouse Setting",
//       icon: "warehouse",
//       link: "/warehouse-setting",
//     },
//   ];

//   onResize() {
//     this.windowWidth = window.innerWidth;
//   }

//   mounted() {
//     this.$nextTick(() => {
//       this.windowWidth = window.innerWidth;
//       window.addEventListener("resize", this.onResize);
//     });
//   }
// }
// </script>
