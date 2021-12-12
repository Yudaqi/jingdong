
<template>
  <div>
    <div class="wrapper">
      <StaticPart />
      <NearBy />
    </div>
    <Docker />
  </div>
</template>
<script>
import StaticPart from './StaticPart'
import NearBy from './NearBy'
import Docker from './Docker'
export default {
  name: 'Home',
  components: { StaticPart, NearBy, Docker }
}
</script>
<style lang="scss">
.wrapper {
  position: absolute;
  left: 0;
  top: 0;
  right: 0;
  padding: 0 0.18rem 0.01rem 0.18rem;
  bottom: 0.49rem;
  overflow-y: auto;
}
</style>
