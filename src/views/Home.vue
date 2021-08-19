<template>
  <div class="wrapper">
    <section class="box" v-for="(item, index) in items" :key="index">
      <header>
        <ItemTitle class="summarybox-item-title" :title="item.title" />
      </header>
      <ItemPicture @click="showDetails" class="infobox-item-picturebox" :image="item.picture" />
      <ItemProperties class="infobox-item-properties" :info="item.properties" />
      <ItemDescription class="summarybox-item-description" :description="item.pattern" />
      <ItemNotes class="summarybox-item-notes" :notes="item.notes" />
    </section>
  </div>
</template>

<script>
import { ref } from 'vue'
import { data } from '@/data.js'
import ItemTitle from '@/components/ItemTitle.vue'
import ItemDescription from '@/components/ItemDescription.vue'
import ItemNotes from '@/components/ItemNotes.vue'
import ItemPicture from '@/components/ItemPicture.vue'
import ItemProperties from '@/components/ItemProperties.vue'

export default {
  components: {
    ItemTitle,
    ItemDescription,
    ItemNotes,
    ItemPicture,
    ItemProperties,
  },
  methods: {
    showDetails() {
      console.log('Button clicked')
    },
  },
  setup() {
    const items = ref(data)

    return {
      items,
    }
  },
}
</script>
