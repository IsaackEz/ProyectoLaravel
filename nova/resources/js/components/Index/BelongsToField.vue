<template>
  <div :class="`text-${field.textAlign}`">
    <span>
      <span v-if="field.viewable && field.value" class="no-underline dim text-primary font-bold">
        <!-- <router-link
          :to="{
            name: 'detail',
            params: {
              resourceName: field.resourceName,
              resourceId: field.belongsToId,
            },
          }"
          class="no-underline dim text-primary font-bold"
        > -->
          {{ field.value }}
        <!-- </router-link> -->
      </span>
      <span v-else-if="field.value">{{ field.value }}</span>
      <span v-else>&mdash;</span>
    </span>
  </div>
</template>

<script>
export default {
  props: ['resourceName', 'field'],
}
</script>
