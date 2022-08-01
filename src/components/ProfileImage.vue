<template>
  <img
    :src="imageLink"
    class="w-8 h-8 object-contain rounded-3xl"
    alt="Profile image"
  />
</template>

<script>
export default {
  name: "ProfileImage",

  data() {
    return {
      imageLink: "https://avatars.githubusercontent.com/u/20451520?v=4",
    };
  },
};
</script>
