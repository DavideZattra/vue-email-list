<template>
  <div class="email-list">
    <ul>
      <li v-for="(element, index) in emailList" :key="index">
        {{ element }}
      </li>
    </ul>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'Emaillist',
  data: function(){
    return{
      emailList : [],
    }
  },
  mounted(){
    for (let i=0; i<10; i++){
      axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
      .then( (response) => {
        const result = response.data;
        console.log(result.response);
        this.emailList.push(result.response);
      })

    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
