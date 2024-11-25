<script setup>
const props = defineProps({
  data: {
    type: Object,
    default: null,
  },
})
const form = ref({})
const attrs = useAttrs()
watch(() => attrs.modelValue, (val) => {
  if (val) {
    form.value = {}
  }
})
</script>
<template>
  <hl-form-dialog title="" :model="form">
    <hl-form-item label="">
    </hl-form-item>
  </hl-form-dialog>
</template>
<style lang='scss' scoped>
</style>
