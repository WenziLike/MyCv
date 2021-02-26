<template>
    <section>
        <div class="skills">
            <h2>Skills</h2>
            <ul>
                <li v-for="item in skills" :key="item">
                    <a :href="item.link" target="_blank">{{ item.title }}</a>
                </li>
                <h4 class="skills-sub-title">Transpilators :</h4>
                <hr/>
                <li>
                    <a href="https://webpack.js.org" target="_blank">WebPack</a>
                </li>
                <li><a href="https://gulpjs.com" target="_blank">Gulp</a></li>
                -->
            </ul>
        </div>
        <div class="education">
            <section>
                <h2>Education</h2>
                <h4>Dnipro National Mining University</h4>
                <p>
                    The department of Mine aerology and <br/>
                    a labor safety , 2016
                </p>
                <p>Graduated and worked as a Labor Inspector</p>
            </section>
        </div>
        <div class="languages">
            <section>
                <h2>Languages</h2>
                <ul>
                    <li v-for="item in languages" :key="item">{{ item }}</li>
                </ul>
            </section>
        </div>
    </section>
</template>

<script>
export default {
    inject: ['languages', 'skills'],
}
</script>