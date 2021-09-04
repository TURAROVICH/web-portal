<template>
    <div class="form mx-auto w-4/5 ">
    <div class="flex flex-col ">
    <div class="explain-text">
        Придумайте новый пароль
    </div>
    <input type="text" class="w-full" id="email" placeholder="Пароль">
    <input type="text" class="w-full" id="email" placeholder="Повторите пароль">

    <div  class="btn">
        <span>Подтвердить</span>
    </div>
    </div>

    



    </div>
</template>



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


</style>