<template>
    <FeatureItem theme="hmo">
        <template #pre-item><div class="gradient-hmo"></div></template>
        <template #heading><span class="main-header">ABOUT ME</span></template>
        <div class="main info-gradient">
            <p>I was born and raised in Hermosillo, Sonora and I studied Computer Science at Universidad de Sonora.</p>
            <p>Some of my hobbies are: 
                video games (playing & discussing them, keeping up to date with the latest industry gossip, etc.), modding games, coding, internet, going to the movies and binge watching series & anime.
            </p>
        </div>
    </FeatureItem>

    <FeatureItem theme="skills">
        <template #heading><span class="main-header">SKILLS</span></template>
        <div class="main info-gradient">
            I've been working as a Software Developer since 2017 and in that time I have gained proficiency on different skills such as:
            <p><span class="skill">Python</span></p>
            <p><span class="skill">C#</span></p>
            <p><span class="skill">SQL</span></p>
            <p><span class="skill">Back-end development (Django, ASP.NET, Laravel, etc.)</span></p>
            <p><span class="skill">Front-end development (React, Angular, Vue, etc.)</span></p>
            <p><span class="skill">Android development (Android Studio, Ionic Framework)</span></p>
            <p><span class="skill">Advanced english</span></p>
        </div>
    </FeatureItem>

    <FeatureItem theme="showcase">
        <template #heading><span class="main-header">PERSONAL PROJECTS</span></template>
        <div class="project-showcase">
            <!-- This page -->
            <div class="project">
                <h3 class="header-box">This webpage</h3>
                <div class="info-gradient">
                    Who would've thought!
                    <p>Made with <span class="skill">Vue</span></p>
                </div>
            </div>
            
            <!-- FE Fates Calculator -->
            <div class="project">
                <h3 class="header-box"> <a href="https://robbiehub.github.io/fates-calculator/">Fire Emblem Fates Calculator</a> </h3>
                <div class="info-gradient">
                    A growth rate and maximum stat calculator for Fire Emblem Fates
                    <p>Made with <span class="skill">Vue</span></p>
                    <a href="https://robbiehub.github.io/fates-calculator/">
                        <img class="project-img" src="/docs/assets/images/fates.png" alt="Snapshot of the Fire Emblem Fates Calculator">
                    </a>
                </div>
            </div>

            <!-- WAVExtender -->
            <div class="project">
                <h3 class="header-box"> <a href="https://github.com/robbiehub/WAVExtender">WAVExtender</a></h3>
                <div class="info-gradient">
                    A Python script for extending .wav files with sample chunks
                    <p>Made with <span class="skill">Python</span></p>
                </div>
            </div>
        </div>
    </FeatureItem>
    
</template>

<script>
    import FeatureItem from './FeatureItem.vue'

    export default{
        components: { FeatureItem }
    }
</script>

<style>
p span{
    background-color: #f6a62b;
    padding: 0 5px;
    border-radius: 3px;
}

.main.info-gradient{
    font-size: 1.25em;
    border-style: dotted;
    border-width: 3px 0;
}

.main-header{
    font-size: 2em;
    font-weight: 900;
    color: white;
    -webkit-text-stroke: 1px black;
}

.gradient-hmo{
    /* background: linear-gradient(180deg, #a6aaad, transparent); */
    background: linear-gradient(180deg, #8eafe4, transparent);
    width: 100%;
    height: 100%;
    position: absolute;
}
.gradient-hmo::after{
    content: ' ';
}

.header-box a{
    font-weight: 500;
    color: white;
}

.project-showcase{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

.project{
    /* max-width: 50%; */
    margin-bottom: 1em;
}

.project-img{
    width: 100%;
}
</style>
