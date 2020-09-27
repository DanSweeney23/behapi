<template>
  <div id="drum-container">
        <Key number="1"/>
        <Key number="2"/>
        <Key number="3"/>
        <Key number="4"/>
        <div ></div>
        <Key number="6"/>
        <Key number="7"/>
        <Key number="8"/>
        <Key number="9"/>
  </div>
</template>

<script>
import Key from '../components/Key.vue'
export default {
    name: 'Drum',
    components: {
        Key
    }
}
</script>

<style scoped>
    #drum-container {
        display:grid;
        grid-template-rows: 200px 200px 200px;
        grid-template-columns: 200px 200px 200px;
        grid-gap: 20px;
    }
</style>