<template>
  <div v-if="data" class="home-advisor-section">
    <template v-if="data.image_alignment === 'Left'">
      <img :src="data.image.url" :alt="data.image.filename" />
      <div class="home-content">
        <h2>{{ data.title_h2 }}</h2>
        <p>
          {{ data.description }}
        </p>
        <NuxtLink aria-current="page" class="btn secondary-btn" to="/">{{
          data.call_to_action.title
        }}</NuxtLink>
      </div>
    </template>
    <template v-else>
      <div class="home-content">
        <h2>{{ data.title_h2 }}</h2>
        <p>
          {{ data.description }}
        </p>
        <NuxtLink aria-current="page" class="btn secondary-btn" to="/">{{
          data.call_to_action.title
        }}</NuxtLink>
      </div>
      <img :src="data.image.url" :alt="data.image.filename" />
    </template>
  </div>
</template>

<script>
export default {
  props: ['data'],
}
</script>
