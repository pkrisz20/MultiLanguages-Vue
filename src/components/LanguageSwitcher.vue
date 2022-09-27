<template>
    <div class="changer">
        <select @change="setLocale($event)" v-model="$i18n.locale">
            <option v-for="(lang, i) in $i18n.availableLocales" :key="`Lang${i}`" :value="lang">{{ lang }}</option>
        </select>
    </div>
</template>

<script>
export default {
    name: 'LanguageSwitcher',
    methods: {
        setLocale(event) {
            this.$i18n.locale = event.target.value;
            this.$router.push({ params: { lang: event.target.value } });
        }
    }
}
</script>

<style scoped lang="scss">

</style>
