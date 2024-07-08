<script setup>
import { useI18n } from 'vue-i18n'
import { useGlobalState } from '../store'
const { openSettings } = useGlobalState()


const { t } = useI18n({
    messages: {
        en: {
            copyright: "Copyright"
        },
        zh: {
            copyright: "版权所有"
        }
    }
});

</script>

<template>
    <div>
        <n-divider class="footer-divider" />
        <div style="text-align: center; padding: 20px">
            <n-text depth="3">
                {{ t('copyright') }} &copy; 2023-{{ new Date().getFullYear() }} {{ openSettings.copyright }}
                <br>
                萌ICP备<a href="https://icp.gov.moe/?keyword=20240520" target="_blank">20240520</a>号
            </n-text>
        </div>
    </div>
</template>


<style scoped>
.footer-divider {
    margin: 0;
    padding: 0 var(--x-padding);
}
</style>
