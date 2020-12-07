<template>
  <div>
      <b-card>
    <b-form @submit="onSubmit" >
           <h3>Contact Us </h3>

      <b-form-group>
         <b-form-input
          type="name"
          required
          placeholder="Enter name"
          class="mb-4"
        ></b-form-input>
        <b-form-input
          type="email"
          required
          placeholder="Enter email"
          class="mb-4"
        ></b-form-input>
            <b-form-input
          type="Phone"
          required
          placeholder="Enter Phone"
          class="mb-4"

        ></b-form-input>
         <b-form-textarea
      id="textarea"
      placeholder="Enter Message..."
   
    ></b-form-textarea>
      </b-form-group>


      <b-button type="submit" variant="primary">Submit</b-button>
    </b-form>
      </b-card>
  </div>
</template>

<script>
  export default {
    data() {
      return {
     
      }
    },
    methods: {
      onSubmit(evt) {
        evt.preventDefault()
        alert("form validation success");
      },
      
    }
  }
</script>