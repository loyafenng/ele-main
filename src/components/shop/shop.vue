<template> 
  <div>shop</div>
</template>

<script type="text/ecmascript-6">
import {urlParse} from '../../common/js/util';
const ERR_OK = 0;
export default {
  data() {
    return {
      seller: {
        id: (() => {
          let queryParam = urlParse();
          console.log(queryParam);
          return queryParam.id;
        })()
      }
    };
  },
  created() {
    this.$http.get('/api/foods').then((response) => {
      response = response.body;
      if (response.errno === ERR_OK) {
        console.log(response.data);
      }
    });
  }
};
</script>

<style lang="stylus" rel="stylesheet/stylus">
    @import '../../common/stylus/mixin.styl';
</style>
