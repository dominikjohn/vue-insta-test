<script>
import {Stories} from "vue-insta-stories";

export default {
    name: 'ExerciseIntro',
    components: {Stories},
    props: {
        moduleName: String
    },
    methods: {
        finishIntro() {
            alert('Intro finished!')
        },
    },
    computed: {
        introduction_slides() {
            return [
                "https://picsum.photos/1080/1920",
                "https://picsum.photos/1080/1921",
                "https://picsum.photos/1080/1919",
                "https://picsum.photos/1080/1922",
                "https://picsum.photos/1080/1923",
                "https://picsum.photos/1080/1918",
            ]
        }
    }
}
</script>

<template>
    <div>
        <Stories :stories="introduction_slides" interval="8000" class="ig-stories" @all-stories-end="finishIntro"/>
    </div>
</template>

<style scoped lang="scss">
.ig-stories {
  position: absolute;
  height: 100vh;
  width: 100vw;
  top: 0;
  left: 0;
  z-index: 50;
}

@media (min-width: 768px) {
  .ig-stories {
    position: relative;
    height: 730px;
    width: 410px;
  }
}
</style>
