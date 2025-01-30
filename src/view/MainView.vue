<template>
  <div class="main">
    <Kv />
    <About />
    <Skill />
    <Suspicious />
    <Project />
    <Ending />
  </div>
</template>
<script>
  import Kv from "../components/Main/KvSec.vue";
  import About from "../components/Main/AboutSec.vue";
  import Skill from "../components/Main/SkillSec.vue";
  import Suspicious from "../components/Main/SuspiciousSec.vue";
  import Project from "../components/Main/ProjectSec.vue";
  import Ending from "../components/Main/EndingSec.vue";


  export default {
    components: {
      Kv,
      About,
      Skill,
      Suspicious,
      Project,
      Ending,
    },
  }
</script>