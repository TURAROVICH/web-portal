<template>
    <div class="cards">
          <div  class="card">
            <div class="fio">
              <div class="profil">
                <img src="@/assets/imgs/test/test.png" alt="">
                <div class="fullname">Никита Зайцев</div>
              </div>
              <div class="type">Заказчик</div>
            </div>
            <div class="date">
              <div class="years">14.07.2020</div>
              <div class="hours">00:36</div>
            </div>
            <div class="city">
              Салават
            </div>
            <div @click="blocked_modal=true" class="deteails">
                <svg width="8" height="14" viewBox="0 0 8 14" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M1 13L7 7L1 1" stroke="#6A7489" stroke-opacity="0.5" stroke-width="1.125" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>

            </div>
          </div>
          <div class="card">
            <div class="fio">
              <div class="profil">
                <img src="@/assets/imgs/test/test.png" alt="">
                <div class="fullname">Никита Зайцев</div>
              </div>
              <div class="type">Заказчик</div>
            </div>
            <div class="date">
              <div class="years">14.07.2020</div>
              <div class="hours">00:36</div>
            </div>
            <div class="city">
              Салават
            </div>
            <div class="deteails">
                <svg @click="blocked_modal=true" width="8" height="14" viewBox="0 0 8 14" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M1 13L7 7L1 1" stroke="#6A7489" stroke-opacity="0.5" stroke-width="1.125" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>

            </div>
          </div>
            <Blocked v-if="blocked_modal" @close="blocked_modal=false" />
        </div>
</template>

<script>
import Blocked from '../../components/customers-page/blocked.vue'
export default {
    data:()=>({
        blocked_modal:false
    }),
    components:{
        Blocked
    }
}
</script>

<style lang="scss" scoped>
.cards{


  .card{
    display: grid;
    grid-template-columns: 2fr 1fr 1fr .4fr;
    padding: 16px 0 16px 16px;
    background: #FAFAFC;
    &:nth-child(2n){
      background: #fff;
    }
    >div:nth-child(2),>div:nth-child(3),>div:nth-child(4){
      border-left: 1px solid rgba(106, 116, 137, 0.3);
    }
    .deteails{
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .date{
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      margin-left: 17px;
      .years{
        /* Caption/Regular */

        font-family: Nunito;
        font-style: normal;
        font-weight: normal;
        font-size: 14px;
        line-height: 18px;
        /* identical to box height, or 129% */

        display: flex;
        align-items: center;
        text-align: center;
      }
      .hours{
        /* Small/Regular */

          font-family: Nunito;
          font-style: normal;
          font-weight: normal;
          font-size: 12px;
          line-height: 16px;
          display: flex;
          align-items: center;
          text-align: center;

          /* Text/Secondary */

          color: rgba(106, 116, 137, 0.5);
      }
    }
    .city{
      /* Caption/Regular */

        font-family: Nunito;
        font-style: normal;
        font-weight: normal;
        font-size: 14px;
        line-height: 18px;
        /* identical to box height, or 129% */

        display: flex;
        align-items: center;
        text-align: center;
        justify-content: center;
        /* Text/Primary */

        color: #252A36;
    }
    .fio{
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 24px 0 0 ;
       .type{
          max-width:150px;
          height: 22px;
          padding: 0 10px;
          /* Text/Quaternary */
          background: rgba(106, 116, 137, 0.1);
          border-radius: 100px;
        }
     
    }
  }
}

</style>