<template>
    <div class="wecome">
            <div class="loader-inner pacman">
          <div>1</div>
          <div>2</div>
          <div>3</div>
          <div>4</div>
          <div></div>
        </div>
    </div>
</template>
<script>
import {savaToLocal} from '../../common/js/store';
    export default {
        mounted() {
            setTimeout(() => {
                this.$router.push({
                    name: 'welfare'
                });
                savaToLocal('gank', 'wecome', true);
            }, 2000);
        }
    };
</script>
<style lang="stylus" rel="stylesheet/stylus">
    @import './wecome.styl';
</style>
