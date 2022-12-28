<template>
  <div class="Layer">
    <div class="LayerHeader">
      <slot name="header" />
    </div>
    <div class="LayerContent">
      <slot name="content" />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import router from "@/router";
import Stack from "@/components/Stack.vue";

export default defineComponent({
  name: "Layer",
  components: {
    Stack,
  },
  setup(props) {},
});
</script>
