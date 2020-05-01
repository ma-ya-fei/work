<template>
  <main>
    <section>
        <Conter></Conter>
        <Curriculum v-show="state"></Curriculum>
    </section>
  </main>
</template>

<script>
import Conter from "../conter/Conter.vue"
import Curriculum from "../curriculum/Curriculum.vue"
export default {
    data: function() {
        return {
            state:false,
        }
       
    },
    name:"Main",
    components:{
        Conter,
        Curriculum
    }
}

</script>