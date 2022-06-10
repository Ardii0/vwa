<template>
  <div class="flex overflow-hidden min-h-screen flex-row">
    <layout-sidebar :mobile-opened="sidebarMobileOpened" />
    <div
      style="background-color: rgb(234, 234, 234)"
      class="flex max-h-screen flex-col w-full"
    >
      <layout-appbar @onmenuclickedmobile="onmenuclickedmobile" />
      <div
        v-if="sidebarMobileOpened"
        @click="sidebarMobileOpened = false"
        style="z-index: 2; top: 60px"
        class="w-full fixed opacity-50 left-0 right-0 bottom-0 bg-black"
      ></div>

      <div class="flex flex-col p-4 overflow-auto">
        <div
          v-if="navTitle"
          class="w-full rounded-md flex flex-row items-center bg-white "
        >
          <button @click="onNavBack" v-if="!noBack" class="rounded-full">
            <b-icon class="hover:text-black" icon="arrow-left"></b-icon>
          </button>
          <span class="ml-3 text-xl font-normal">{{ navTitle }}</span>
        </div>

          <slot />
        <!-- <div class=" mt-2 p-2 rounded-lg bg-white">
        </div> -->
      </div>
    </div>
    
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";
import { Watch, Prop } from "vue-property-decorator";

@Component
export default class LayoutContainer extends Vue {
  @Prop({ type: [Boolean], default: false })
  noBack!: boolean;
  @Prop({ type: [String] })
  navTitle!: string;

  onNavBack() {
    this.$router.back();
  }

  sidebarMobileOpened = true;
  onmenuclickedmobile() {
    this.sidebarMobileOpened = !this.sidebarMobileOpened;
  }
  windowWidth = null as any;

  @Watch("windowWidth")
  resizeHandler(newVal: any) {
    if (newVal > 1140) {
      this.sidebarMobileOpened = false;
    }
  }

  onResize() {
    this.windowWidth = window.innerWidth;
  }

  mounted() {
    this.$nextTick(() => {
      this.windowWidth = this.windowWidth = window.innerWidth;
      window.addEventListener("resize", this.onResize);
    });
  }
}
</script>
