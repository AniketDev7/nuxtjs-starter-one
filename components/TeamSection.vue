<template>
  <div class="about-team-section">
    <div v-if="data" class="team-head-section">
      <h2>{{ data.title_h2 }}</h2>
      <p>
        {{ data.description }}
      </p>
    </div>
    <div class="team-content">
      <template v-for="index in data.employees">
        <div :key="index.name" class="team-details">
          <img :src="index.image.url" :alt="index.name" />
          <div class="team-details">
            <h3>{{ index.name }}</h3>
            <p>{{ index.designation }}</p>
          </div>
        </div>
      </template>
    </div>
  </div>
</template>

<script>
export default {
  props: ['data'],
}
</script>
