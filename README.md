### Hi there 👋
<h1>这是一个测试网站</h1>

<style>input::-ms-clear,
input::-ms-reveal {
    display: none; /* 去除ie、edge丑陋的显示密码图标*/
}
/**{*/
/*    border: 1px solid red;*/
/*}*/
span{
    position: relative;

}

form{
    text-align: center;
}

label .userName{
    position: relative;
    left: 12px;
}

label .userPassword{
    position: relative;
    left: -10px;
}

#userName{
    position: relative;
    left: 5px;
}

.box img{
    width: 20px;
    position: relative;
    top: 6px;
    left: 209px;
    cursor: pointer;
}

input .username .userPassword{
    color: gray;
    border: #7dc5eb;
}

  #submit{
      width: 80px;
    background: #afdfe4;
      position: relative;
      top: 10px;
      left: 26px;
}</style>

<form class="box" action="#" method="Post">
    <label for="userName" class="username">用户名 </label><input type="text" name="userName" id="userName" value="请输入用户名"><br>
    <img src="../image/eyeClose.png" id="eyeClose">
    <label class="userPassword">密码</label> <input type="password" name="userPassword" id="userPassword" value="请输入密码"><br>
    <input type="submit" value="登录" id="submit">
</form>

<script>
    const pwd = document.getElementById('userPassword');
    const img = document.getElementById('eyeClose');
    const input = document.querySelectorAll('input');
    let flag = 0;

    img.onclick = function () {
        if (flag==0){
            img.src = "../image/eyeOpen.png";
            pwd.type="text";
            flag=1;
        }
        else {
            img.src = "../image/eyeClose.png";
            pwd.type="password";
            flag=0;
        }
    }
    input[0].onclick = function () {
        if(this.value==='请输入用户名')
        {
            this.value='';
            this.style.color='black';
        }
    }

    input[0].onblur = function () {
        if(this.value==='')
        {
            console.log(this.value);
            this.value='请输入用户名';
            this.style.color='gray';
        }
    }

    input[1].onfocus = function () {

        if(this.value==='请输入密码')
            this.value='';
        this.style.color="black";
        if (pwd.type=='password') {
            pwd.type='password';
        }
        else {
            pwd.type = 'text';
        }
    }
    input[1].onblur = function () {
        if(this.value==='')
        {
            this.style.color='gray';
            this.value='请输入密码';
            pwd.type='text';
        }
    }
    input[2].onmousemove = function (){
        this.style.background = '#94d6da';
    }
    input[2].onmouseleave= function (){
        this.style.background = '#afdfe4';
    }




</script>

<!--
**Kisa-Dong/Kisa-Dong** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
