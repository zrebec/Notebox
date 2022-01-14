<template>
  <ul class="infobox-item-properties smaller">
    <li class="infobox-item-property" v-for="(object, index) in info" :key="index">
      <span class="infobox-item-title" v-show="object.name">{{ object.name }}:</span>
      <span v-if="object.type === 'rating'">
        <span v-for="(v, k) in object.value" :key="k">{{ object.icon }}</span>
      </span>
      <span v-else>
        <span>{{ object.value }}</span>
      </span>
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    info: {
      type: Array,
      default: () => {
        return [
          {
            name: '',
            value: 'Produkt neobsahuje zatiaľ žiadne vlastnosti',
            type: 'string',
            icon: '',
          },
        ]
      },
    },
  },
}
</script>
