<template>
    <section>
        <h2>Tell Us about you</h2>
         <div >
            <label for="address" class="label-style">type your good name</label>
            <br/>
            <textarea 
            type="text"
            id="address"
            class="input-style"
            />
        </div>
        <h4>your gender</h4>
            <div class="mb-2">
                <label for="male" class="label-style">male</label>
               
                <input 
                type="radio"
                value="male"
                id="name"
                class="input-style"
                v-model="formValues.gender"
                />
            </div>
          <div mb-2>
            <label for="female" class="label-style">female</label>
          
            <input 
            type="radio"
            value="female"
            id="female"
            class="input-style"
            v-model="formValues.gender"
            />
        </div>
        
       
    </section>
</template>

<script>
    export default {
       name:'About',
       data(){
        return{
            formValues:{
                gender:''
            }
        }
       } 
    }
</script>

<style  scoped>
.info{
    font-weight: bold;
    font-size:40px;
    margin: 20px;
}
 .input-style{
    font-size:20px;
    border-radius: 10px;
    outline:none;
    border:1px solid green;
    padding: 5px 10px;
    margin: 10px 0;
 }
 .label-style{
    font-weight: bold;
    font-size:14px;
    margin-right: 10px;
 }
.mb-2{
    margin-bottom: 10px;
}
</style>
