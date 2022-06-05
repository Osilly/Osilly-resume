<!-- 社交 -->

<template>
    <div class="social" :style="{ 'font-size': size + 'em' }">
        <!-- github -->
        <a :style="{ color: color }" :href="social['github'] || 'https://github.com/Osilly'" target="_blank">
            <a-icon type="github" />
        </a>
        <!-- twitter -->
        <a :style="{ color: color }" :href="social['twitter'] || 'https://twitter.com/Osilly6'" target="_blank">
            <a-icon type="twitter" />
        </a>
        <!-- linkedin -->
        <a :style="{ color: color }"
            :href="social['linkedin'] || 'https://www.linkedin.com/in/%E6%96%87%E8%BD%A9-%E9%BB%84-691ba5227/'"
            target="_blank">
            <a-icon type="linkedin" />
        </a>
    </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import { mapGetters } from 'vuex';

@Component({
    components: {
    },
    props: {
        color: String,
        size: Number,
    },
    computed: {
        ...mapGetters(['social']),
    },
})
export default class Social extends Vue {
}
</script>

<style scoped lang="scss">
.social {
    &>* {
        margin: 0.5em;
    }
}
</style>

