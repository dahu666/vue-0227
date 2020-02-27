<template>
    <div class="hello">
        <h1>{{ msg }}</h1>
        <div v-html="msg1" :id="id" />
        <div>{{ number+12 }}</div>
        <p v-if="seen">现在你看得到我</p>
        <div v-n="4"></div>
        <div :class="[a1,a2]">
            我接你{{money}},你还我{{a}},还欠我{{money -a}}
        </div>
        <div :class="{a1:a3}">
            我接你{{money}},你还我{{a}},还欠我{{b}}
        </div>
    </div>
</template>
<script>
    export default {
        name: 'HelloWorld',
        props: {
            msg: String
        },
        data() {
            return {
                msg1: '<span style="color:red;">hello world</span>',
                id: 'txt',
                number: 1,
                seen: true,
                money: 100,
                a: 10,
                a1: 'test-1',
                a2: 'tst-2',
                a3:true
            }

        },
        computed: {
            b: function () {
                return this.money - this.a
            }
        }
    }
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

    h3 {
        margin: 40px 0 0;
    }

    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        display: inline-block;
        margin: 0 10px;
    }

    a {
        color: #42b983;
    }
</style>
