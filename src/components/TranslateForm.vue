<template>
  <div id="translateForm" class="row">
    <div style="margin:0 auto">
      <form class="well form-inline" v-on:submit="formSubmit">
         <input class="form-control" type="text" placeholder="输入需要翻译的内容" v-model="textToTranslate" style="margin: 10px">
         <select class="form-control" style="margin:0 10px" v-model="language">
             <option value="en">English</option>
             <option value="ru">Russian</option>
             <option value="ko">Korean</option>
             <option value="ja">Janpanese</option>
         </select>
         <input class="btn btn-primary" type="submit" value="翻译" style="margin:10px">
    </form>
    </div>
  </div>
</template>

<script>


export default {
  name: 'translateForm',
  data(){
    return{
        textToTranslate:'',
        language:'en'
    }
  },
  methods:{
    formSubmit:function(e){
        this.$emit("formSubmit",this.textToTranslate,this.language);   //把子组件传递给根组件
        e.preventDefault();
    }
  }
}
</script>

<style>

</style>
