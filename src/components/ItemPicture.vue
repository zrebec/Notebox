<template>
  <div>
    <img class="infobox-item-picturebox-image" :src="require(`@/static/${image}`)" alt="item.title" />
  </div>
</template>

<script>
export default {
  props: {
    image: {
      type: String,
    },
  },
}
</script>
