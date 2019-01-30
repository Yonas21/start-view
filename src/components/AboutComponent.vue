<template>
    <div id="about">
        <span v-once> Message: {{message}}</span>
        <p>Using v-html directive: <span style = "color: green" v-html="message"></span></p>
        <hr/>
        <button @click="showSome" :disabled="check">Submit</button>
        <hr>
        <span v-if="seen">This block should be seen.</span>
        <ol>
            <li v-for="(data,index) in users" :key="index">{{data.name}}</li>
        </ol>

        <!--<div class="container">-->
        <!--<label for="username" class="v-label">User Name</label>-->
        <!--<input type="text" class="form-control" v-model="name">-->
        <!--</div>-->
        <div class="container-fluid">
            <ul class="list-group">
                <li class= "list-group-item active">User Names</li>
                <li class= "list-group-item" v-for="item in items"> {{item}}}</li>
            </ul>
        </div>

        <div class="container">
            <p>The Original user name: {{userName}}</p>
            <p>The Reversed user name: {{reversedUserName}}</p>
        </div>
    </div>
</template>

<script>
    /*eslint-disable */

    //Object.freeze(object)
    export default {
        name: 'about',
        data() {
            return {
                seen:true,
                check:true,
                message: 'This is the message from Angular.',
                users:[
                    {name:'Yonas'},
                    {name: 'Same'},
                    {name:'Mike'},
                    {name:'Hiskel'}
                ],
                items:[
                    "welcome to html",
                    "style ur page ",
                    "make it interactive with js",
                    "try some frameworks",
                    "Angular",
                    "Express",
                    "React"
            ],
                userName:'Lanzini'
            }
        },
        methods:{
            showSome(){
                console.log("welcome to vue event handling")
            },

            reversedUserName:function () {
                //reverse the userName from the data item above
                return this.userName.split('').reverse().join('')
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

    ol {
        font-size: medium;
    }

    ol li {
        list-style-type:lower-alpha;
        display:block;
        color: crimson;
    }
</style>
