<template>
  <div
    style="z-index: 5; background-color: #28ae86"
    class="flex justify-between lg:justify-end pl-3 pr-10 items-center w-full sticky min-w-full top-0"
  >
    <button
      class="flex lg:hidden"
      style="background: none; outline: none; border: 0px"
      @click="onMenuClickedMobile()"
    >
      <b-icon class="cursor-pointer font-bold" icon="menu"> </b-icon>
    </button>
    <div class="flex justify-center items-center flex-row">
      <b-dropdown position="is-bottom-left" class="" aria-role="list">
        <template #trigger>
          <div
            class="flex my-3 rounded-full cursor-pointer justify-center items-center flex-row"
            style="background-color: #3277aa; width: 60px; height: 60px"
          >
            <span class="text-xl font-bold text-white"> TF </span>
          </div>
        </template>
        <b-dropdown-item disabled>
          <div class="w-full flex justify-center align-center flex-col">
            <span class="text-black font-bold text-lg">Talenta Figan</span>
            <span class="mt-1">talenta@gmail.com</span>
          </div>
        </b-dropdown-item>
        <b-dropdown-item aria-role="listitem">
          <div class="flex justify-start align-center flex-row">
            <b-icon icon="account-circle"> </b-icon>
            <span class="ml-2">Account Setting</span>
          </div>
        </b-dropdown-item>
        <b-dropdown-item aria-role="listitem">
          <div class="flex justify-start align-center flex-row">
            <b-icon icon="logout-variant"> </b-icon>
            <span class="ml-2">Sign Out</span>
          </div>
        </b-dropdown-item>
      </b-dropdown>
    </div>
  </div>
</template>

// <script>
// import Vue from "vue";
// import Component from "vue-class-component";

// @Component
// export default class LayoutHeader extends Vue {
//   onMenuClickedMobile() {
//     this.$emit("onmenuclickedmobile");
//   }
// }
// </script>
