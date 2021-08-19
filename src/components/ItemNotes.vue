<template>
  <ul>
    <li v-for="(note, index) in notes" :key="index" class="summarybox-item-note">
      {{ note }}
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    notes: {
      type: Array,
      default: () => {
        return ['Produkt neobsahuje žiadne poznámky']
      },
    },
  },
}
</script>
