<template>
    <div class="form mx-auto w-4/5 ">
    <div v-if="!sended" class="flex flex-col ">
    <div class="explain-text">
        Введите свой адрес электронной почты ниже, и мы отправим вам ссылку для сброса пароля.
    </div>
    <input type="text" class="w-full" id="email" placeholder="Email">
    <div @click="sended=true" class="btn">
        <span>Восстановить</span>
    </div>
    <div @click="$router.push('/auth/login/customer')" class="btn btn-reg">
        <span>Войти</span>
    </div>
    </div>

    <div v-else class="flex flex-col justify-center">
        <div class="text-center explain-text">
            Email отправлен!
        </div>
        <svg class="mx-auto" width="92" height="92" viewBox="0 0 92 92" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path fill-rule="evenodd" clip-rule="evenodd" d="M46 0C20.5955 0 0 20.5955 0 46C0 71.4045 20.5955 92 46 92C71.4045 92 92 71.4045 92 46C92 20.5955 71.4045 0 46 0ZM74.9592 34.834C76.5244 33.2749 76.5294 30.7423 74.9703 29.1771C73.4113 27.612 70.8786 27.607 69.3135 29.166L39.6001 58.7633L25.8229 45.0399C24.2577 43.4808 21.7251 43.4858 20.166 45.051C18.607 46.6161 18.612 49.1488 20.1771 50.7078L36.7772 67.243C38.3381 68.7978 40.8622 68.7978 42.423 67.243L74.9592 34.834Z" fill="#2CC84D"/>
        </svg>
        <div class="explain-text">
            Перейдите по ссылке в электронном письме, которое мы отправили, чтобы завершить сброс пароля.
        </div>

        <div @click="$router.push('/auth/login/customer')" class="to-log">
            Вернуться ко входу
        </div>

    </div>



    </div>
</template>

<script>
export default {
    data:()=>({
        sended:false
    })
}
</script>

<style lang="scss" scoped>
input{
padding: 16px;
outline: none;
height: 56px;
background: #FFFFFF;
border: 1px solid rgba(106, 116, 137, 0.3);
box-sizing: border-box;
border-radius: 16px;
margin: 16px 0;
}
.explain-text{
    /* Caption/Regular */
    margin: 32px 0;
font-family: Nunito;
font-style: normal;
font-weight: normal;
font-size: 14px;
line-height: 18px;
/* or 129% */

text-align: center;

color: #000000;
}

input[type=text]{
padding: 16px;
outline: none;
height: 56px;
background: #FFFFFF;
border: 1px solid rgba(106, 116, 137, 0.3);
box-sizing: border-box;
border-radius: 16px;
margin: 16px 0;
}

.btn{
    margin: 32px 0 16px 0 ;
    display: flex;
justify-content: center;
align-items: center;
padding: 16px 28px;
height: 60px;
width: 100%;
background: #2CC84D;
border-radius: 16px;
span{
    font-family: Nunito;
    font-style: normal;
    font-weight: bold;
    font-size: 18px;
    line-height: 25px;
    /* identical to box height */

    text-align: center;

    /* General/White */

    color: #FFFFFF;
}
}

.btn-reg{
    background: transparent;
    border: none;
    span{
       /* Buttons/Large */

        font-family: Nunito;
        font-style: normal;
        font-weight: bold;
        font-size: 18px;
        line-height: 25px;
        /* identical to box height */

        text-align: center;

        /* Text/Primary */

        color: #252A36;
    }
}
.to-log{
    /* Buttons/Large */

font-family: Nunito;
font-style: normal;
font-weight: bold;
font-size: 18px;
line-height: 25px;
/* identical to box height */

text-align: center;

/* Accent/Primary */

color: #2CC84D;
}

</style>