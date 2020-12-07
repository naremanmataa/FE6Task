<template>
  <div>
      <b-card-group>
         <b-row  v-for="(category, index) in currentUser"
            :key="index" class="mb-4">

              <b-col class="m-2 cardStyle"  >

           <b-card class="text-center" :header= category.name>
     <h4> Email:</h4> {{category.email}}
     <h4>   Phone: </h4>{{category.phone}}

         </b-card>
             </b-col>
    </b-row>         

</b-card-group>

  </div>
</template>

<script>
  export default {
       data() {
      return {
          currentUser:[],
      }
       },
    methods: {
       getUsers(){
           this.axios.get('https://jsonplaceholder.typicode.com/users').then((response) => {
               this.currentUser=response.data
            console.log(response.data)
          })
 
       }
      },
      mounted(){
          this.getUsers();
      }
  }
</script>