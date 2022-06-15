<template>
    <section>
        <div class="info">general Information</div>
        <div>
            <label for="name" class="label-style">type your good name</label>
            <br/>
            <input 
            type="text"
            id="name"
            class="input-style"
            />
        </div>
            <div>
                <label for="name" class="label-style">when were you born?</label>
                <br/>
                <input 
                type="date"
                id="name"
                class="input-style"
                />
            </div>
          <div>
            <label for="name" class="label-style">How old are you?</label>
            <br/>
            <input 
            type="text"
            id="name"
            class="input-style"
            />
        </div>
          <div>
            <label for="name" class="label-style">where we can send you emails</label>
            <br/>
            <input 
            type="text"
            id="name"
            class="input-style"
            />
        </div>
    </section>
</template>

<script>
    export default {
        name:'Information'
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

    margin-bottom: 12px;
   
    
 }

</style>
