<template>
<div class="container">
  <about  class="p-4" />
  <users />
  <contact  class="p-4" />

</div>
</template>
<script>
import users from "./users"
import about from "./about"
import contact from "./contact"
export default {
  components: {
     contact,
     about,
     users
    },
}
</script>
