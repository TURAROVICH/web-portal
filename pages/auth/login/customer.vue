<template>
    <div class="form mx-auto w-4/5 flex flex-col ">
        <input type="text" class="w-full" id="email" placeholder="Логин, почта или телефон">
        <input type="text" class="w-full" placeholder="Пароль">
        <checkbox desc="Запомнить меня"/>
        <div class="btn">
            <span>Войти</span>
        </div>
        <div class="forgot-password">Забыли пароль?</div>

        <div class="not-acc">
            Нет аккаунта?
        </div>

        <div @click="$router.push('/auth/register/customer')" class="btn btn-reg">
            <span>Зарегистрироваться</span>
        </div>
        <div class="about-reg">
            Регистрация займет меньше минуты
        </div>
    </div>
</template>


<style lang="scss" scoped>

.not-acc{
    font-family: Nunito;
font-style: normal;
font-weight: normal;
font-size: 16px;
line-height: 24px;
text-align: center;
/* identical to box height, or 150% */
margin: 48px 0 16px 0;
display: flex;
align-items: center;
justify-content: space-between;
/* Text/Secondary */

color: rgba(106, 116, 137, 0.5);
&::before{
    content: "";
    display: inline-block;
    width: 93.5px;
    height: 2px;
    background: rgba(106, 116, 137, 0.5);
}
&::after{
    content: "";
    display: inline-block;
    width: 93.5px;
    height: 2px;
    background: rgba(106, 116, 137, 0.5);
}
}

.forgot-password{
    font-family: Nunito;
font-style: normal;
font-weight: normal;
font-size: 14px;
line-height: 18px;
/* identical to box height, or 129% */

text-align: center;

/* Text/Primary */

color: #252A36;

}
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
    background: #FFFFFF;
    border: 1px solid #2CC84D;
    span{
        color: #2CC84D;
    }
}

.about-reg{
    /* Caption/Regular */

font-family: Nunito;
font-style: normal;
font-weight: normal;
font-size: 14px;
line-height: 18px;
text-align: center;
color: rgba(106, 116, 137, 0.5);
}
</style>