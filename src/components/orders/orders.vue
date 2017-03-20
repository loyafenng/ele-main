<template> 
<div>
  <div>orders</div>
  <v-menu footerIndex="3"></v-menu>
</div>
</template>

<script type="text/ecmascript-6">
import menu from '../banner/banner';
export default {
  components: {
    'v-menu': menu
  }
};
</script>

<style lang="stylus" rel="stylesheet/stylus">
    @import '../../common/stylus/mixin.styl';
</style>
