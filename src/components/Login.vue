<template>
  <h1>Login Page</h1>
  <div class="container">
    <form action="">
        <div class="form-group">
                <input type="text" name="name" id="name" class="" autocomplete="off" required/>
                <label for="name">Username</label>
            </div>

            <div class="form-group">
                <input type="password" name="password" id="password" class="" autocomplete="off" required />
                <label for="password">Password</label>
            </div>

            <button type="submit" class="btn">Login</button>
    </form>
  </div>
</template>

<script >
import { ref } from 'vue';
export default {
    name: "login"
}

setup(){
    const username = ref(null);
    const password = ref();

    let collect_username = ()=>{
        
    }
    return {username,password}
};

</script>   

<style >

body{
    font-family: 'Mulish', sans-serif;
    background-color: #7158e2;
    color: #fff;
    height: 100vh;

    display: flex;
    justify-content: center;
    align-items: center;

    margin: 0;
    overflow: hidden;
}
    .container{
    background-color: rgba(0,0,0,0.4);
    padding: 20px 40px;
    border-radius: 5px;
}

.container h1{
    text-align: center;
    margin-bottom: 30px;
}

.form-group{
    width: 300px;
    margin: 20px 0 40px;

    position: relative;
}

.form-group input{
    width: 100%;
    background-color: transparent;
    border:none;
    border-bottom: 2px solid #fff;
    font-size: 18px;
    color: #fff;
    padding: 15px 0;

}

.form-group input:focus{
    outline: 0;
    border-bottom-color: #4287f5 ;
}

.btn{
    width: 100%;
    background-color: #4287f5;
    font-family: inherit;
    font-size: 16px;
    padding: 15px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

.btn:focus{
    outline: 0;
}

.btn:active{
    transform: scale(0.98);
}

.text{
    margin-top: 30px;
}

.container a{
    /*position: ;*/
    text-decoration: none;
    color: #4287f5;
}

.form-group label{
    position: absolute;
    top: 15px;
    left: 0;

}

.form-group label span{
    display: inline-block;
    transition: all 0.3s ease;
    
}

.form-group input:focus + label span,
.form-group input:valid + label span{
    color: #4287f5;
    transform: translateY(-30px);
}
</style>