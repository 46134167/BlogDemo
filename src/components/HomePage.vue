<template>
    <div id="outer-container" style="width:80%;height:95%;margin:0 auto">

        <div class="basic_info" style="width:30%;margin-top:0px;">
            <p align="left" style="font-size:32px;margin-left:10px;font-weight:bold">TIANLE YANG</p>
            <a-divider style="margin-top:-30px;"/>
            <p align="left" style="color:blue;margin-top:-20px;margin-left:10px;font-size:18px;font-weight:bold;"> Input Your Title Here</p>
        </div>
        <a-layout>
            <a-layout-header>
                <a-menu
                        v-model:selectedKeys="selectedKeys"
                        theme="dark"
                        mode="horizontal"
                        :style="{ lineHeight: '64px' }"
                >
                    <a-menu-item key="1" @click="RoutePage(1)">HOME</a-menu-item>
                    <a-menu-item key="2" @click="RoutePage(2)">RESEARCH</a-menu-item>
                    <a-menu-item key="3" @click="RoutePage(3)">PUBLICATIONS</a-menu-item>
                    <a-menu-item key="4" @click="RoutePage(4)">SERVICES</a-menu-item>
                    <a-menu-item key="5" @click="RoutePage(5)">SUPERVISION</a-menu-item>
                    <a-menu-item key="6" @click="RoutePage(6)">TEACHING</a-menu-item>
                </a-menu>
            </a-layout-header>
            <a-layout-content>
<!--                <div id="innercontainer" style="width:98%;height:100%;margin:0 auto">-->
<!--                    <div id="introduction" align="left" >-->
<!--                        <p style="font-size:24px;margin-top:10px;">Introduction</p>-->
<!--                        <p style="font-size:15px;margin-top:-10px;">-->
<!--                            Xiaotian Dai is a research associate at the University of York, UK. He received a PhD degree from University of York in 2019 (with Best Thesis).-->
<!--                            He joined real-time systems group in 2015 as a PhD research student, supervised by Prof. Alan Burns. His PhD research involves cooperatively design of control system and real-time task scheduling for Cyber-Physical Systems (CPS), where various flexible scheduling task models are proposed and implemented to investigate the scheduling impact on control performance.-->
<!--                            He received a M.Sc. in Control Systems from the University of Sheffield in 2014, and a B.Sc. in Automatic Control in 2011. He serves as a reviewer and a PC member for many top real-time, embedded and design automation conferences.-->
<!--                        </p>-->
<!--                    </div>-->
<!--                    <a-divider/>-->

<!--                    <a-divider/>-->
<!--                </div>-->
                <router-view></router-view>
            </a-layout-content>
            <a-layout-footer>
            </a-layout-footer>
        </a-layout>
    </div>
</template>

<script>
    import {ref} from 'vue';
    export default {
        name: 'HomePage',
        setup() {
            return {
                selectedKeys: ref(['1']), //chose home by default
            };
        },
        methods:{
            RoutePage(key) {
                console.log(key)
                switch (key){
                    case 1:
                        this.$router.replace('/Home')
                        break
                    case 2:
                        this.$router.replace('/Research')
                        break
                    case 3:
                        this.$router.replace('/Publications')
                        break
                    case 4:
                        this.$router.replace('/Services')
                        break
                    case 5:
                        this.$router.replace('/Supervision')
                        break
                    case 6:
                        this.$router.replace('/Teaching')
                        break

                }
                // if(this.selectedKeys[0] === "1")
                //     this.$router.replace('/Home')
                // else
                //     this.$router.replace('/Research')
            },
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
