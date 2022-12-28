<template>
  <div class="Main">
    <div class="Main--content">
      <LayerContent>
        <template #header>
          <Stack contentId="about" title="About" />
        </template>
        <template #content>
          <div>test</div>
        </template>
      </LayerContent>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import router from "@/router";
import LayerContent from "@/components/Layer.vue";
import Stack from "@/components/Stack.vue";

export default defineComponent({
  name: "Main",
  components: {
    Stack,
    LayerContent,
  },
  setup(props) {},
});
</script>
