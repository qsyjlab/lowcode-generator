<template>
  <div class="designer-container">
    <div class="designer-container__header"></div>
    <div class="designer-container__body">
      <div class="designer-container__operate"></div>
      <div class="designer-container__render"></div>
      <div class="designer-container__setting"></div>
    </div>
  </div>
</template>
<script setup lang="ts">
interface IProps {
  height?: string;
}
withDefaults(defineProps<IProps>(), {
  height: "100vh",
});
</script>
<style lang="scss">
// * {
//   outline: 1px solid red;
// }
.designer-container {
  height: 100vh;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;

  &__header {
    height: 48px;
    box-sizing: border-box;
    flex-shrink: 0;
    border-bottom: 1px solid #e5e5e5;
  }

  &__body {
    flex: auto;
    display: flex;
    justify-content: space-between;
  }

  &__operate {
    width: 300px;
  }

  &__render {
    flex: auto;
    height: 100%;
    background-color: aqua;
  }

  &__setting {
    width: 300px;
  }
}
</style>
