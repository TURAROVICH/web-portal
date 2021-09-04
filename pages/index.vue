<template>
  <div class="main">
      <div class="profile">
        <div>
            <img src="@/assets/imgs/test/profile.png" alt="">
        </div>
        <div>
          <div class="full-name">Администратор</div>
        </div>
      </div>


      <div class="request">
        <div class="title">Заявки</div>
        <div class="search-container">
          <div class="search">
              <input type="text" placeholder="Поиск">
              <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M19 19L14.65 14.65M17 9C17 13.4183 13.4183 17 9 17C4.58172 17 1 13.4183 1 9C1 4.58172 4.58172 1 9 1C13.4183 1 17 4.58172 17 9Z" stroke="#6A7489" stroke-opacity="0.3" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
          </div>
           <div class="search" style="width:251px;">
              <input ref="date" type="text" placeholder="Выбрать период">
            <svg v-if="svg" width="20" height="22" viewBox="0 0 20 22" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M14 1V5M6 1V5M1 9H19M3 3H17C18.1046 3 19 3.89543 19 5V19C19 20.1046 18.1046 21 17 21H3C1.89543 21 1 20.1046 1 19V5C1 3.89543 1.89543 3 3 3Z" stroke="#252A36" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>

          </div>
        </div>

        <div class="desc-card">
          <div class="desc">
            <div class="title">ФИО</div>
            <svg width="20" height="18" viewBox="0 0 20 18" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M1 1H14M1 5H10M1 9H7M11 9L15 5M15 5L19 9M15 5V17" stroke="#6A7489" stroke-opacity="0.3" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>

          </div>
          <div class="desc">
            <div class="title">Дата, время</div>
            <svg width="20" height="18" viewBox="0 0 20 18" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M1 1H14M1 5H10M1 9H7M11 9L15 5M15 5L19 9M15 5V17" stroke="#6A7489" stroke-opacity="0.3" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>

          </div>
          <div class="desc">
            <div class="title">Город</div>
            <svg width="20" height="18" viewBox="0 0 20 18" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M1 1H14M1 5H10M1 9H7M11 9L15 5M15 5L19 9M15 5V17" stroke="#6A7489" stroke-opacity="0.3" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>

          </div>
          <div></div>
        </div>

        <div class="cards">
          <div @click="exec_modal=true" class="card">
            <div class="fio">
              <div class="profil">
                <img src="@/assets/imgs/test/test.png" alt="">
                <div class="fullname">Никита Зайцев</div>
              </div>
              <div class="type">Исполнитель</div>
            </div>
            <div class="date">
              <div class="years">14.07.2020</div>
              <div class="hours">00:36</div>
            </div>
            <div class="city">
              Салават
            </div>
            <div class="deteails">
                <svg width="8" height="14" viewBox="0 0 8 14" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M1 13L7 7L1 1" stroke="#6A7489" stroke-opacity="0.5" stroke-width="1.125" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>

            </div>
          </div>
          <div @click="cust_modal=true"  class="card">
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
                <svg width="8" height="14" viewBox="0 0 8 14" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M1 13L7 7L1 1" stroke="#6A7489" stroke-opacity="0.5" stroke-width="1.125" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>

            </div>
          </div>
        </div>


        
      </div>

    <customerModal v-if="cust_modal" @close="cust_modal=false"/>
    <executorModal v-if="exec_modal"  @close="exec_modal=false"/>
  </div>
</template>

<script>
import customerModal from '@/components/main-page/customer-modal.vue'
import executorModal from '@/components/main-page/executor-modal.vue'
export default {
  data:()=>({
    svg:true,
    cust_modal:false,
    exec_modal:false
  }),
  mounted(){
    let t = this
    this.$refs.date.onfocus=function(e){
      this.type = 'datetime-local'
      this.focus()
      t.svg = false
    }
  },
  components:{
    customerModal,executorModal
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
      .profil{
        display: flex;
        align-items: center;
        gap:10px;
      
        .fullname{
          font-family: Nunito;
          font-style: normal;
          font-weight: bold;
          font-size: 16px;
          line-height: 24px;
          color: #252A36;
        }
        >img{
          width: 40px;
          height: 40px;
          border-radius: 50%;
        }
      }
    }
  }
}


.request{
  width: 100%;
  padding: 24px;
  background: #FFFFFF;
  border-radius: 16px;
  margin: 69px 0 74px 0;
  .desc-card{
    width: 100%;
    height: 72px;
    padding: 18px 80px;
    background: #FFFFFF;
    border-radius: 8px;
    margin: 42px 0 0 0;
    display: grid;
    grid-template-columns: 2fr 1fr 1fr .1fr;
    grid-column-gap: 20px;
    .desc{
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .desc:nth-child(2),.desc:nth-child(3){
      border-left:1px solid rgba(106, 116, 137, 0.3);
      padding: 0 0 0 20px;
    }
  }
  .search-container{
    width: 100%;
    padding: 24px 0;
    border-bottom:  2px solid #F1F3F8;
    display: flex;
    align-items: center;
    gap: 24px;;
    .search{
      display: flex;
      width: 412px;
      height: 48px;/* BG/Primary */
      padding: 15px;
      background: #FFFFFF;
      gap: 10px;
      align-items: center;
      /* Text/Tertiary */

      border: 1px solid rgba(106, 116, 137, 0.3);
      box-sizing: border-box;
      border-radius: 16px;
      input{
        width:  100%;
        border: none;
        outline: none;
      }

    }
  }
  .title{

    font-family: Raleway;
    font-style: normal;
    font-weight: 800;
    font-size: 20px;
    line-height: 24px;
    /* identical to box height, or 120% */

    font-feature-settings: 'pnum' on, 'lnum' on, 'liga' off;

    /* Text/Primary */

    color: #252A36;

  }
}
.profile{
  width:  100%;
  position: relative;
  & > div:first-child{
    background: #EBEBEB;
  }
  &>:last-child{
    background: #fff;
  }
  &>div{
    width: 100%;
    height: 160px;
  }
  img{
    width: 140px;
    height: 140px;
    border-radius: 50%;
    position: absolute;
    top: calc(50% - 70px);
    left:55px;
  }
  .full-name{
    font-family: Nunito;
    font-style: normal;
    font-weight: bold;
    font-size: 24px;
    line-height: 30px;
    /* identical to box height */

    padding: 94px 36px 0px 54px;
    color: #000000;
  }
}
.main{
  width: 100%;

}
</style>