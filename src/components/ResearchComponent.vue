<template>
    <div id="innercontainer" style="width:98%;height:100%;margin:0 auto">
        <div id="ResearchInterest" align="left" >
            <p style="font-size:24px;margin-top:10px;">Research Interests</p>
            <ul>
                <li>Real-time systems, including scheduling and allocation on single- and multi-cores, and timing predictable hardware;</li>
                <li>Flexible and feedback-based methods for task/network scheduling in CPS;</li>
                <li>Control-scheduling co-design and design automation of CPS;</li>
            </ul>
        </div>
        <a-divider/>

        <div id="ResearchProjects" align="left" >
            <p style="font-size:24px;margin-top:10px;">Research Projects</p>
            <div id="Project1">
                <a-space direction="vertical">
                    <a-typography-link style="font-size:20px;margin-top:10px;" href="https://antdv.com" target="_blank">
                        <right-outlined></right-outlined>
                        Put Project Intro and Maybe Links Here

                    </a-typography-link>
                    <a-typography-text strong style="font-size: 15px">some brief descriptions</a-typography-text>
                </a-space>
                <p style="margin-top: 10px">
                    The applications and resources (processors, networks and memory) for real-time systems are becoming ever more complex to understand,
                    control and maintain. This has led to research into building statistical models of systems and adaptive policies based on these statistical models.
                </p>
            </div>
        </div>

        <a-divider/>
    </div>
</template>

<script>
    import { RightOutlined } from '@ant-design/icons-vue';
    export default {
        name: 'HomeComponent',
        methods:{

        },
        components: {
            RightOutlined,
        },
    }
</script>