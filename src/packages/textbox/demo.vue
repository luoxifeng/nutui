<template>
    <div class="textbox-demo">
        <!-- <h4>示例</h4> -->
        <h4>默认用法</h4>
         <nut-textbox v-model="val"></nut-textbox>
        <h4>自定义高度:100px</h4>
        <nut-textbox :txtAreaH="100" :maxNum="300"></nut-textbox>

        <h4>自定义提示语</h4>
        <nut-textbox :placeText="'请填写详细情况请填写详细情况'"></nut-textbox>
        

        <h4>自定义字数限制</h4>
        <nut-textbox :maxNum="100"></nut-textbox>
        

        <h4>限制字数不可超出</h4>
        <nut-textbox :switchMax="true" :maxNum="10" :txtAreaH="100" textBgColor="#efefef"></nut-textbox>
        

        <h4>字数超出报错</h4>
        <nut-textbox :maxNum="10" :txtAreaH="100"  @errorFunc="overLength" ></nut-textbox>
        

        <h4>自定义文本框背景色</h4>
        <nut-textbox :switchMax="true" :maxNum="10" :txtAreaH="100" textBgColor="#feefef"></nut-textbox>

        <h4>不显示字数限制</h4>
        <nut-textbox :limitShow="false" :maxNum="10" ></nut-textbox>
       
        <h4>输入回调返回文字</h4>
        <nut-textbox  :maxNum="10" txtAreaH="100" @inputFunc="inputText" ></nut-textbox>
    </div>
</template>

<script>
export default {
    data(){
        return{
            val: ''
        }
    },
    methods:{
        overLength(){
            alert("字数超出");
        },
        inputText(val){
           alert(val);
        }
    }
}
</script>
