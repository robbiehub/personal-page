<template>
    <FeatureItem :reversed="true">
        <template #heading>About Me</template>
        <p>I was born and raised in Hermosillo, Sonora and I studied Computer Science at Universidad de Sonora.</p>
        <p>Some of my hobbies are: 
            video games (playing & discussing them, keeping up to date with the latest industry gossip, etc.), modding games, coding, internet, going to the movies and binge watching series & anime.
        </p>
    </FeatureItem>

    <FeatureItem>
        <template #heading>Skills</template>
        I've been working as a Software Developer since 2017 and in that time I have gained proficiency on different skills such as:
        <p><span class="skill">Python</span></p>
        <p><span class="skill">C#</span></p>
        <p><span class="skill">SQL</span></p>
        <p><span class="skill">Back-end development (Django, ASP.NET, Laravel, etc.)</span></p>
        <p><span class="skill">Front-end development (React, Angular, Vue, etc.)</span></p>
        <p><span class="skill">Android development (Android Studio, Ionic Framework)</span></p>
        <p><span class="skill">Advanced english</span></p>

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
</style>
