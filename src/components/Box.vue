<template>
  <div class="col-md-4 information">
    <div class="main-content">
      <div>
        <h3>{{ title }}</h3>
        <h4>{{ value }}</h4>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Box",
  props: {
    title: {
      type: String,
    },
    value: {
      type: Number,
    },
  },
};
</script>
