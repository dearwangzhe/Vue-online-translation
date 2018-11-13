<template>
  <div id="translateOutput">
    <p>{{translatedText}}</p>
  </div>
</template>

<script>


export default {
  name: 'translateOutput',
  props:[
    "translatedText"                    //父组件传给子组件
  ],
}
</script>

<style>

</style>
