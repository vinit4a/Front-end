<template>
    <base-dialog v-if="inputIsInvalid" title="Invalid Input" @click="confirmError">
    <template #default> 
          <p>Unfortunately, at least one input  value is invalid.</p>
          <p>Please check all inputs and make sure you enter at least a few charactors into  each input field. </p>
    </template>

    <template #actions> 
        <base-button @click="confirmError">Okay</base-button>
        <p></p>
    </template>
    </base-dialog>
    <base-card>
    <form @submit.prevent="submitData">
        <div class="form-control">
        <label for="title">Title</label>
        <input type="text" name="title" id="text" ref="titleInput" />
        </div>

         <div class="form-control">
        <label for="Description">Description</label>
        <textarea name="description" id="description" rows="3" ref="descInput"></textarea>
        </div>

         <div class="form-control">
        <label for="link">Link</label>
        <input type="url" name="link" id="text" ref="linkInput"/>
        </div>

        <div>
            <base-button type="submit" >Add Resource</base-button>
        </div>
    </form>

    </base-card>
</template>

<script>

export default {
  
    inject:['addResource'],
    data(){
        return{
            inputIsInvalid:false,
        }
    },
    methods:{
        submitData() {
              const enteredTitle = this.$refs.titleInput.value;
              const enteredDescription = this.$refs.descInput.value;
              const enteredurl = this.$refs.linkInput.value;

              if(enteredTitle.trim() === '' || enteredDescription.trim() ==='' || enteredurl.trim()===''){
                  this.inputIsInvalid = true;
                  return;
              }

              this.addResource(enteredTitle,enteredDescription,enteredurl);
        },
        confirmError(){
            this.inputIsInvalid = false;
        }
    }
}
</script>

<style scoped>
    label {
  font-weight: bold;
  display: block;
  margin-bottom: 0.5rem;
}

input,
textarea {
  display: block;
  width: 100%;
  font: inherit;
  padding: 0.15rem;
  border: 1px solid #ccc;
}

input:focus,
textarea:focus {
  outline: none;
  border-color: #3a0061;
  background-color: #f7ebff;
}

.form-control {
  margin: 1rem 0;
}
</style>