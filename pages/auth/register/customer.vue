<template>
    <div class="form  flex flex-col ">
       <!-- <v-select :options="options" id="select" class="select"  v-model="selected"></v-select>
        -->
        <div  class="select">
            <span :class="{'small':selected}">Я являюсь</span> 
            <div class="selected" v-if="selected" v-html="selected"></div>
            <svg @click="modal=!modal" width="14" height="8" viewBox="0 0 14 8" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M1 1L7 7L13 1" stroke="#252A36" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>

            <div v-if="modal" class="drop-down-content">
                <div v-for="i in options" :key="i" @click="selected=i;modal=false" v-html="i" class="variant"></div>
            </div>

        </div>
        <div class="flex items-center gap-2 relative">
            <input type="text"   placeholder="Логин">
                <svg class="s-1"  style="" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2 12 2C6.47715 2 2 6.47715 2 12C2 17.5228 6.47715 22 12 22Z" stroke="#6A7489" stroke-opacity="0.3" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M9.08984 8.99999C9.32495 8.33166 9.789 7.7681 10.3998 7.40912C11.0106 7.05015 11.7287 6.91893 12.427 7.0387C13.1253 7.15848 13.7587 7.52151 14.2149 8.06352C14.6712 8.60552 14.9209 9.29151 14.9198 9.99999C14.9198 12 11.9198 13 11.9198 13" stroke="#6A7489" stroke-opacity="0.3" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M12 17H12.01" stroke="#6A7489" stroke-opacity="0.3" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
                <div   v-if="info1" class="card absolute ">
                   <div>Не менее 8 символов</div>
                   <div>Обязательно содержание цифр и букв</div>
                </div>

        </div>
            <div v-if="sel==='Юридическое лицо'" class="flex items-center gap-2 relative">
            <input type="text"   placeholder="Рабочая почта">
                <svg class="s-2"  style="" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2 12 2C6.47715 2 2 6.47715 2 12C2 17.5228 6.47715 22 12 22Z" stroke="#6A7489" stroke-opacity="0.3" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M9.08984 8.99999C9.32495 8.33166 9.789 7.7681 10.3998 7.40912C11.0106 7.05015 11.7287 6.91893 12.427 7.0387C13.1253 7.15848 13.7587 7.52151 14.2149 8.06352C14.6712 8.60552 14.9209 9.29151 14.9198 9.99999C14.9198 12 11.9198 13 11.9198 13" stroke="#6A7489" stroke-opacity="0.3" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M12 17H12.01" stroke="#6A7489" stroke-opacity="0.3" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
                <div   v-if="info2" class="card absolute ">
                   <div>рабочий электронный адрес</div>
                </div>

        </div>

         <div v-if="sel==='Физическое лицо'" class="flex items-center gap-2 relative">
                <input type="text"   placeholder="Телефон">
                <svg class="s-2"  style="" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2 12 2C6.47715 2 2 6.47715 2 12C2 17.5228 6.47715 22 12 22Z" stroke="#6A7489" stroke-opacity="0.3" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M9.08984 8.99999C9.32495 8.33166 9.789 7.7681 10.3998 7.40912C11.0106 7.05015 11.7287 6.91893 12.427 7.0387C13.1253 7.15848 13.7587 7.52151 14.2149 8.06352C14.6712 8.60552 14.9209 9.29151 14.9198 9.99999C14.9198 12 11.9198 13 11.9198 13" stroke="#6A7489" stroke-opacity="0.3" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M12 17H12.01" stroke="#6A7489" stroke-opacity="0.3" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
                <div   v-if="info2" class="card absolute ">
                   <div>Телефон номер.</div>
                </div>
         </div>

        <div class="flex items-center gap-2 ">
            <input v-model="pass1" type="password"   placeholder="Пароль">
 

        </div>
        <input v-model="pass2" type="password"  placeholder="Повторите пароль">
        <div v-if="coincide" class="flex gap-2 items-center">
            <svg width="12" height="9" viewBox="0 0 12 9" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M11.3332 1L3.99984 8.33333L0.666504 5" stroke="#5DD13A" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
            <span style="color:#2CC84D;">Пароли совпадают</span>

        </div>
        <div class="checkboxes flex flex-col gap-6 my-8 ">
            <checkbox desc="Согласен на <nuxt-link to='#' style='color:#2CC84D;margin-left:4px;'>обработку и хранение персональных данных</nuxt-link> "/>
            <checkbox desc="Согласен c <nuxt-link to='#' style='color:#2CC84D;margin-left:4px;'>Пользовательским соглашением</nuxt-link> "/>
            <checkbox desc="Согласен получать информационные письма от сервиса"/>
        </div> 
        <div class="btn cursor-pointer">
            <span>Войти</span>
        </div>

        <div class="about-reg w-11/12 cursor-pointer">
            Отмена
        </div>
    </div>
</template>

<script>
import vSelect from 'vue-select'
import "vue-select/src/scss/vue-select.scss";
export default {
    data:()=>({
        pass1:'',
        pass2:'',
        coincide:false,
        info1:false,
        info2:false,
        mail:false,

        selected:'',
        modal:'',
        options:[
            'Юридическое лицо',
            'Физическое лицо',
            'ИП',
            `<span style='color:#2CC84D;'>НКО</span>`,
            'Самозанятый'
        ]
    }),
    watch:{
        pass2(){
            if(this.pass1.length > 7){
                if(this.pass1 === this.pass2){
                   this.coincide = true
                }else{
                    this.coincide = false
                }
            }else{
                this.coincide = false
            }
        }
    },
    mounted(){
        window.addEventListener('mousemove',(e)=>{
           if(e.target.matches('.s-1')){
               this.info1 =true
           }else {
               this.info1 =false
           }
           if(e.target.matches('.s-2')){
               this.info2 =true
           }else {
               this.info2 =false
           }
        })
    },
    computed:{
        sel(){
            return this.selected
        }
    },
    components:{
        vSelect
    }
    
}
</script>

<style lang="scss" scoped>

.select{
width: 88%;
height: 56px;
position: relative;
/* BG/Primary */

background: #FFFFFF;
/* Text/Tertiary */

border: 1px solid rgba(106, 116, 137, 0.3);
box-sizing: border-box;
border-radius: 16px;
display: flex;
align-items: center;
justify-content: space-between;
padding: 0 25px 0 16px;
span{
    font-family: Nunito;
font-style: normal;
font-weight: normal;
font-size: 16px;
line-height: 24px;
/* identical to box height, or 150% */


/* Text/Secondary */

color: rgba(106, 116, 137, 0.5);

}
.drop-down-content{
    position: absolute;
    bottom: -240px;
    left: 0;
    width: 100%;
    background: #fff;
    min-height: 240px;
    z-index: 100;
    /* BG/White */

    background: #FFFFFF;
    box-shadow: 0px 2px 8px rgba(79, 79, 118, 0.12);
    border-radius: 8px;

}
.variant{
font-family: Nunito ;
font-style: normal;
font-weight: normal;

    padding: 12px 16px;
font-size: 16px;
line-height: 24px;
/* identical to box height, or 150% */

display: flex;
align-items: center;

/* Text/Primary */

color: #252A36;
height: 48px;
width: 100%;
&:hover{
    background: #FAFAFC;;
}
}
.small{
    font-size: 12px;
line-height: 16px;
position: absolute;
top: 2px;
left: 16px;
/* Text/Secondary */

color: rgba(106, 116, 137, 0.5);
}


}




.card{
    width: 144px;
    height: 66px;
box-shadow: 0px 2px 10px rgba(0,0,0,.1);
background: #FFFFFF;
border-radius: 8px;
right: -130px;
z-index: 50;
bottom: 0px;
padding: 10px;
div{
    /* Tiny/Regular */

font-family: Nunito;
font-style: normal;
font-weight: normal;
font-size: 10px;
line-height: 14px;

/* Text/Primary */
margin: 2px 0;
color: #252A36;

}
}
.form{
    margin-left: 10%;
}
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
width: 470px;
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
    width: 430px;
    display: flex;
justify-content: center;
align-items: center;
padding: 16px 28px;
height: 60px;
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
font-family: Nunito;
font-style: normal;
font-weight: bold;
font-size: 18px;
line-height: 25px;
/* identical to box height */

text-align: center;
color: #252A36;
margin: 30px 0 0 0;

}
@media screen and (min-width:1450px) {
    input{
        width:530px;
    }
    .btn{
        width:94%;
    }
    .about-reg{
        width: 94%;
    }

}
@media screen and (min-width:1650px) {
    input{
        width:570px;
    }
}
@media screen and (max-width:1450px) {
    input{
        width:470px;
    }

}


@media (max-width:1700px) {
    .select{
        width: 570px;
    }
}

@media (max-width:1300px) {
    input{
        width: 367px;
    }
    .btn{
        width:367px;
    }
    .about-reg{
        width: 367px;
    }
    .select{
        width: 367px;
    }

}

@media (max-width:1500px) {
     input{
         width: 94%;
    }
    .btn{
       width: 94%;
    }
    .about-reg{
         width: 94%;
    }
    .select{
        width: 94%;
    }
}
</style>