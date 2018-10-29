<template>
  <div class="list">
    <div class="title">{{ title }}</div>
    <div class="list">
      <div class="list-item" v-for="item in items" :key="item.name">
        <slot name="shape" v-bind="item"></slot>
        <slot name="color" v-bind="item"></slot>
        <slot v-bind="item"></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['title', 'items']
}
</script>

