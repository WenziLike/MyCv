<template>
    <div class="flex-auto">
        <div class="card br-5 m-2">
            <section>
                <h2>{{ positionName }}</h2>
                <h3>{{ whatAreSearchingFor }}</h3>
                <hr/>
                <h4>JOB OBJECTIVE . . .</h4>
                <div class="text">
                    <p v-for="item in jobObjective" :key="item">
                        {{ item }}
                    </p>
                </div>
            </section>
        </div>
        <div class="card br-5 m-2">
            <section>
                <h3>MY PROJECTS</h3>
                <hr/>
                <div class="text">
                    <p>
                        <span class="check-mark" v-html="checkMark"></span>
                        Freelance Full Stack Engineer
                        <a href="https://profizno.com/" target="_blank">ProfiZNO.com</a>
                        (Ukraine)/ Designing a full stack from 0 to final result of a web
                        page. Used are technologies such as
                        <span class="mark">Php, Php Mailer, Vanilla JS, Gulp, SCSS</span>.
                        plus setting up <span class="mark">Google Analytics</span>
                    </p>
                    <p>
                        <span class="check-mark" v-html="checkMark"></span>
                        Vue Steppers
                        <a href="https://wenzilike.github.io/Vue-Stepper/" target="_blank">
                            10 Quick-Fire Vue Interview Questions
                        </a>
                        (Poland),<br/>
                        Used are technologies such as
                        <span class="mark">Vue 2 Options Api</span> Useful to read...))
                    </p>
                    <p>
                        <span class="check-mark" v-html="checkMark"></span>
                        Java Script Constructor built on the principles of OOP and
                        S.O.L.I.D.
                        <a href="https://constructor.slavamur.com/" target="_blank"> Go to Constructor </a>
                        (SPB), Used are technologies such as
                        <span class="mark">Webpack, Using "VanillaJS"</span> , without
                        frameworks.
                    </p>

                    <p>
                        <span class="check-mark" v-html="checkMark"></span>
                        Blog News
                        <a href="https://blog.slavamur.com/" target="_blank"> Go to Blog </a>
                        (SPB), Used are technologies such as <br>
                        <span class="mark">
                            Vue js , VueX , Axios Promise based
                            HTTP client for the browser and node.js
                        </span> ,
                        registration, login, pagination, Setting and Edit page,popular tags
                    </p>
                </div>
            </section>
        </div>
        <div class="card br-5 m-2">
            <section>
                <h3>OTHER ACTIVITIES</h3>
                <hr/>
                <div class="text">
                    <p v-for="item in otherActivities" :key="item">
                        {{ item }}
                    </p>
                </div>
            </section>
        </div>
    </div>
</template>

<script>
export default {
    inject: [
        'checkMark',
        'positionName',
        'whatAreSearchingFor',
        'jobObjective',
        'otherActivities'
    ]
}
</script>