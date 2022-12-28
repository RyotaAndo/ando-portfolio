<template>
  <div class="Stack" :id="contentId">
    <div class="StackHeader">
      <div class="StackHeaderLeft">
        <div class="StackHeaderLeft__front">
          <div class="Stack__title--txt">
            {{ title }}
          </div>
        </div>
        <div class="StackHeaderLeft__back"></div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Stack",
  props: {
    contentId: {
      type: String,
      required: false,
    },
    title: {
      type: String,
      required: true,
    },
    titleStyle: {
      type: String,
      required: false,
    },
  },
});
</script>

<style lang="scss" scoped></style>
