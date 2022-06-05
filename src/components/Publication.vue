<template>
    <div class="content" id="publication">
        <ModuleHeader :title="publication.header.title" :sub-title="publication.header.subtitle" />
        <a-timeline>
            <a-timeline-item data-aos="fade-in" v-for="card in publication.cards" v-bind:key="card.title">
                <a-card class="publication-card" :bordered="true" style="width: 100%">
                    <template slot="title">
                        <a class="title" href="card.link" target="_blank">{{ card.title }}</a>
                    </template>
                    <a-row type="flex" justify="left" align="top">
                        <a-col flex="2.5" class="col" :xs="24" :sm="24" :md="24" :lg="12" :xl="10">
                            <img width="100%" height="100%" data-aos="fade-in" class="avatar" draggable="false"
                                v-bind:src="card.image" />
                        </a-col>
                        <a-col flex="1"></a-col>
                        <a-col flex="5" class="col" :xs="24" :sm="24" :md="24" :lg="12" :xl="10">
                            <vue-markdown>{{ card.md }}</vue-markdown>
                        </a-col>
                    </a-row>

                </a-card>
            </a-timeline-item>
        </a-timeline>
    </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import ModuleHeader from '@/components/module/ModuleHeader.vue';
import { Module } from '@/api/user_interface';


@Component({
    components: {
        ModuleHeader,

    },
    computed: {
        publication(): Module {
            // 使用getModule方法获取该模块的配置内容
            return this.$store.getters.getModule('publication');
        },
    },
})

export default class Publication extends Vue {
}



</script>

<style scoped lang="scss">
@import '../styles/variable';

.publication-card {
    .title {
        width: 100%;
        font-size: 1rem;
        overflow: scroll;
        margin: 0;
        font-weight: bold;
        color: rgb(136, 133, 133);
    }

    .sub-title {
        width: 100%;
        font-size: .5rem;
        display: block;
        margin-top: .5rem;
    }
}

.description {
    * {
        margin-right: 4px;
    }
}
</style>