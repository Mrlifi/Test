<template>
    <div class="hello">
        <span>{{childmessage}}</span><i>&nbsp;&nbsp;===&nbsp;&nbsp;</i><span>{{msg}}</span>
    </div>
</template>
<script>
export default {
    props: {
        childmessage: {
            type: String,
        }
    },
    name: 'HelloWorld',
    data() {
        return {
            msg: '',
        }
    },
    watch: {
        childmessage: {
            immediate: true, //代表在wacth里声明了childmessage这个方法之后立即先去执行handler方法
            handler(val) {
                this.msg = val;
            }
        }
    },
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h1 {
    color: red;
}

h2 {
    color: yellow;
}
</style>