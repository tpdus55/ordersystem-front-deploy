<!-- template안에는 html문법이 나오고 -->
<template>
    <div>HTML 화면</div>
    <!-- 화면 내에서 변수를 사용할때에는 {{}} 사용 -->
    <div>{{name}}</div>
    <div>{{email}}</div>
    <!-- @click : 이벤트요소 -->
    <button @click="test()">test함수 호출</button>

</template>
<!-- script안에는 export default{}가 나와야함 -->
<script>
export default{
    // 컴포넌트 이름
    name: "TestVue",
    // 컴포넌트 내에서 사용할 변수 정의
    data(){
        return{
            name: "hongildong",
            email: "hong@naver.com"
        }
    },
    // 컴포넌트 내에서 사용할 함수(메서드) 정의
    methods: {
        test(){
            console.log("hello world");
            // vue에서 전역변수에 접근할때에는 template에서는 this키워드 없이 접근이 가능하지만, 메서드에서는 this키워드 필요
            console.log(this.name);
            console.log(this.email);
        }
    }
}
</script>
<style>
</style>