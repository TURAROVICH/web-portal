<template>
    <div class="root">
        <div class="header z-50 fixed top-0 left-0">
            <img src="@/assets/imgs/main/logo.png" alt="">

            <div class="profile">
                <div class="full-name">Администратор</div>
                <img src="@/assets/imgs/main/Avatars.png" alt="" class="profile-img">
            </div>
        </div>

            <div style="margin-top:74px;" class="body min-h-screen w-full flex">
                <div class="nav">
                    <nuxt-link to="/" exact-active-class="active">
                    <div class="nav-link">
                        <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path  d="M7.5 18.3334V10.0001H12.5V18.3334M2.5 7.50008L10 1.66675L17.5 7.50008V16.6667C17.5 17.1088 17.3244 17.5327 17.0118 17.8453C16.6993 18.1578 16.2754 18.3334 15.8333 18.3334H4.16667C3.72464 18.3334 3.30072 18.1578 2.98816 17.8453C2.67559 17.5327 2.5 17.1088 2.5 16.6667V7.50008Z" stroke="#6A7489" stroke-opacity="0.5" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                        </svg>


                        <span >Главная</span>
                    </div>
                    </nuxt-link>
                    <nuxt-link to="/customers/active" active-class="active" >
                    <div class="nav-link">
                        <svg width="20" height="18" viewBox="0 0 20 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path stroke="#6A7489" d="M14.1666 16.5V14.8333C14.1666 13.9493 13.8155 13.1014 13.1903 12.4763C12.5652 11.8512 11.7174 11.5 10.8333 11.5H4.16665C3.28259 11.5 2.43474 11.8512 1.80962 12.4763C1.1845 13.1014 0.833313 13.9493 0.833313 14.8333V16.5M19.1666 16.5V14.8333C19.1661 14.0948 18.9203 13.3773 18.4678 12.7936C18.0153 12.2099 17.3818 11.793 16.6666 11.6083M13.3333 1.60833C14.0503 1.79192 14.6858 2.20892 15.1397 2.79359C15.5935 3.37827 15.8398 4.09736 15.8398 4.8375C15.8398 5.57764 15.5935 6.29673 15.1397 6.88141C14.6858 7.46608 14.0503 7.88308 13.3333 8.06667M10.8333 4.83333C10.8333 6.67428 9.34093 8.16667 7.49998 8.16667C5.65903 8.16667 4.16665 6.67428 4.16665 4.83333C4.16665 2.99238 5.65903 1.5 7.49998 1.5C9.34093 1.5 10.8333 2.99238 10.8333 4.83333Z"  stroke-opacity="0.5" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                        </svg>

                        <span>Заказчики</span>
                    </div>
                    </nuxt-link>
                    <nuxt-link to="/executors/active" active-class="active" >
                        <div class="nav-link">
                        <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path stroke="#6A7489" d="M1.66669 1.66675L13.75 4.58341L15 10.8334L10.8334 15.0001L4.58335 13.7501L1.66669 1.66675ZM1.66669 1.66675L7.98835 7.98842M10 15.8334L15.8334 10.0001L18.3334 12.5001L12.5 18.3334L10 15.8334ZM10.8334 9.16675C10.8334 10.0872 10.0872 10.8334 9.16669 10.8334C8.24621 10.8334 7.50002 10.0872 7.50002 9.16675C7.50002 8.24627 8.24621 7.50008 9.16669 7.50008C10.0872 7.50008 10.8334 8.24627 10.8334 9.16675Z"  stroke-opacity="0.5" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                        </svg>



                        <span>Исполнители</span>
                    </div>
                    </nuxt-link>
                    <nuxt-link to="/feedback/customers" active-class="active" >
                        <div class="nav-link">
                            <svg width="20" height="16" viewBox="0 0 20 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path stroke="#6A7489" d="M18.3334 2.99992C18.3334 2.08325 17.5834 1.33325 16.6667 1.33325H3.33335C2.41669 1.33325 1.66669 2.08325 1.66669 2.99992M18.3334 2.99992V12.9999C18.3334 13.9166 17.5834 14.6666 16.6667 14.6666H3.33335C2.41669 14.6666 1.66669 13.9166 1.66669 12.9999V2.99992M18.3334 2.99992L10 8.83325L1.66669 2.99992"  stroke-opacity="0.5" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                            </svg>


                        <span>Обратная связь</span>
                    </div>
                    </nuxt-link>

                </div>
                <div class="nuxt w-full">
                    <Nuxt/>
                </div>
            </div>

        <div class="footer flex justify-between">
            <div class="flex flex-col gap-2">
                <img width="142" height="72" src="@/assets/imgs/main/Union.png" alt="">
                <div class="about">© 2015-2021 ООО «1Дар» <br> Все права защищены</div>
                <div class="about">Условия пользования</div>
                <div class="about">Политика конфеденциальности</div>
            </div>
            <div class="footer-nav">
                <div class="flex flex-col">
                    <div class="title">Меню</div>
                    <div class="link">Главная</div>
                    <div class="link">Биржа</div>
                    <div class="link">Обучение</div>
                    <div class="link">Мои задания</div>
                    <div class="link">Чат</div>
                    <div class="link">Обратная связь</div>
                    <div class="link">Портфолио</div>
                </div>
                 <div class="flex flex-col">
                    <div class="title">Соцсети</div>
                    <div class="link">VK</div>
                    <div class="link">Facebook</div>
                    <div class="link">Twitter</div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data:()=>({
        color:'#252A36',
        route:'/'
    }),
    computed:{
        r(){
            console.log('kk');
            return this.$route
        }
    }
    
}
</script>

<style lang="scss" scoped>
.root{
    width: 100%;

}
.nuxt{
    background: #E5E5E5;
    padding: 32px 120px 0px 54px;
}
.nav{
    width: 138px;
    min-height: 100vh;
    background: #fff;
    padding: 56px 8px;
    display: flex;
    align-items: center;
    gap: 20px;
    flex-direction: column;
    &-link{
        width:122px;
        height: 56px;  /* Text/Quaternary */
        background: rgba(106, 116, 137, 0.1);
        border-radius: 12px;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        gap:5.67px;
        span{
            font-family: Nunito;
            font-style: normal;
            font-weight: bold;
            font-size: 12px;
            line-height: 16px;
            display: flex;
            align-items: center;
            text-align: center;

            /* Text/Primary */
            color: rgba(106, 116, 137, 0.5);
          
        }
    }
    .active{
        span{
            color:#252A36;
        }
        svg path {
            stroke-opacity: 1;
            stroke:#252A36;
        }
    }

}

.footer{
    width: 100%;
    height: 296px;
    padding: 48px 255px 30px 60px;

    /* Text/Primary */

    background: #252A36;
    .about{
    /* Small/Regular */
    font-family: Nunito;
    font-style: normal;
    font-weight: normal;
    font-size: 12px;
    line-height: 16px;

    /* General/White */

    color: #FFFFFF;

    }
    .about:nth-child(3){
        margin-top: 24px;
    }
    .footer-nav{
        display: flex;
        justify-content: space-between;
        gap:100px;
        .title{
            /* Body/Bold */

        font-family: Nunito;
        font-style: normal;
        font-weight: bold;
        font-size: 16px;
        line-height: 24px;
        /* identical to box height, or 150% */


        /* General/White */

        color: #FFFFFF;
        margin-bottom: 16px;
        }

        .link{
            /* Small/Regular */

        font-family: Nunito;
        font-style: normal;
        font-weight: normal;
        font-size: 12px;
        line-height: 16px;
        display: flex;
        align-items: center;

        /* General/White */

        color: #FFFFFF;
        margin: 4px 0;
        }
    }
}
.header{
    width: 100%;
    min-height: 70px;
    background: #252A36;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 16px 120px 16px 16px;
    .profile{
        width: 150px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        gap:16px;
        .full-name{
            /* Body/Bold */

        font-family: Nunito;
        font-style: normal;
        font-weight: bold;
        font-size: 16px;
        line-height: 24px;
        /* identical to box height, or 150% */


        /* General/White */

        color: #FFFFFF;

        }
        &-img{
            border-radius: 50%;
        }
    }
}
</style>