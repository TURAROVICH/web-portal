<template>
  <div class="main">

      <div class="nuxt-child-link flex">
          <nuxt-link active-class="active-l" to="/feedback/customers">
                <div class="nuxt-l">
                    <span>Заказчики</span>
                </div>
          </nuxt-link>
          <nuxt-link active-class="active-l" to="/feedback/executors">
                <div class="nuxt-l">
                    <span>Исполнители</span>
                </div>
          </nuxt-link>
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

        
        <nuxt-child/>

        
      </div>

  </div>
</template>

<script>

export default {
  data:()=>({
    svg:true,
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
  }
}
</script>


<style lang="scss" scoped>
.nuxt-child-link{
    max-width: 356px;
    margin: 56px auto ;
    background: #FAFAFC;
    border-radius: 10px;
    a{
        border-radius: 10px;
    }
}
.nuxt-l{
display: flex;
flex-direction: column;
justify-content: center;
align-items: center;
padding: 0px 24px;

position: static;
width: 178px;
height: 32px;
left: 2px;
top: 2px;

/* Accent/Primary */

border-radius: 10px;
span{
    font-family: Nunito;
font-style: normal;
font-weight: bold;
font-size: 16px;
line-height: 24px;
/* identical to box height, or 150% */

display: flex;
align-items: center;
text-align: center;
color: #252A36;

}
}
.active-l{
    background: #2CC84D;
    span{
        color: #FFFFFF;
    }
}
.request{
  width: 100%;
  padding: 24px;
  background: #FFFFFF;
  border-radius: 16px;
  margin: 22px 0 74px 0;
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