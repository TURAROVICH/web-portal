<template>
    <div class="modal-container" >
        <div class="modal">
            <div class="close">
                <svg  @click="$emit('close')" width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
                <rect width="32" height="32" rx="10" fill="#6A7489" fill-opacity="0.3"/>
                <path d="M20 8L12 16L20 24" stroke="white" stroke-width="2" stroke-linecap="round"/>
                </svg>
                <h2 class="close-title">Подробнее</h2>

            </div>

            <div class="body">
                <div class="profile">
                    <img width="128" height="128" src="@/assets/imgs/test/profile.png" alt="">
                    <h1 class="title">MAG Interactive</h1>
                </div>

            <h3 class="message">
                Augue donec nec cras sed ac, facilisi enim erat.
            </h3>
            <div class="date">19.07.2021</div>
                
            <div class="desc">
                Lacus, aliquam commodo molestie aliquam. Gravida ante tincidunt est nulla. Mattis malesuada et ultrices quam mauris magna quis facilisis donec. Viverra duis tempus tellus morbi. At feugiat sed sed suspendisse lorem ullamcorper at adipiscing aenean. Faucibus ultrices aliquet morbi purus cursus. Donec viverra mauris adipiscing lectus.
            </div>
            <masked-input
            style="margin:40px 0 16px 0;width:100%;"
            type="text"
            name="phone"
            class="form-control"
            :mask="['+',7,'(', /[1-9]/, /\d/, /\d/, ')', ' ', /\d/, /\d/, /\d/, '-', /\d/, /\d/, /\d/, /\d/]"
            :guide="false"
            placeholder="Номер телефона">
            </masked-input>
            <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='e' required />
                            <label for="e" class="form__label">Email</label>
            </div>

             <button class="btn-1">
                        <span>Прочитано</span>
            </button>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.field{
    max-width: 360px;
}
.btn-1{
                    display: flex;
                    flex-direction: row;
                    justify-content: center;
                    align-items: center;
                    padding: 16px 28px;
                    margin-top: 64px;
                    width: 272px;
                    height: 56px;

                    /* Accent/Primary */

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
.desc{
    /* Body/Regular */

font-family: Nunito;
font-style: normal;
font-weight: normal;
font-size: 16px;
line-height: 24px;
/* or 150% */


/* Text/Primary */

color: #252A36;
width: 70%;
}
.date{
    /* Caption/Regular */

font-family: Nunito;
font-style: normal;
font-weight: normal;
font-size: 14px;
line-height: 18px;
/* identical to box height, or 129% */


/* Text/Secondary */

color: rgba(106, 116, 137, 0.5);
margin: 8px 0 24px 0;
}
.message{
    /* H5/Bold */
font-family: Raleway;
font-style: normal;
font-weight: 800;
font-size: 24px;
line-height: 28px;
font-feature-settings: 'pnum' on, 'lnum' on, 'liga' off;
margin-top: 64px;
/* Text/Primary */

color: #252A36;
}
.modal-container{
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    z-index: 51;
    background:rgba(0,0,0,.2);

    .modal{
        position: fixed;
        height: 100vh;
        width: 70%;
        top: 0;
        right: 0;
        background: #fff;
        z-index: 52;
        opacity: 1;
        overflow-y: scroll;
        .body{
            width: 100%;
            padding: 48px 121px 62px 72px;
            
            .profile{
                display: flex;
                align-items: center;
                .title{
                    /* H3/Bold */

                font-family: Raleway;
                font-style: normal;
                font-weight: 800;
                font-size: 40px;
                line-height: 47px;
                /* identical to box height */

                font-feature-settings: 'pnum' on, 'lnum' on, 'liga' off;

                /* Text/Primary */

                color: #252A36;
                }
            }
        }
        .close{
            min-height: 70px;
            border-bottom:1px solid #F1F3F8;
            display: flex;
            gap: 22px;
            padding: 22px;
            &-title{
                font-family: Raleway;
                font-style: normal;
                font-weight: 800;
                font-size: 24px;
                line-height: 28px;
                font-feature-settings: 'pnum' on, 'lnum' on, 'liga' off;

                /* Text/Primary */

                color: #252A36;
            }
        }
    }

}
input{
    max-width: 360px;
    height: 56px;
    padding: 8px 16px;
    background: #FFFFFF;
    /* Text/Tertiary */

    border: 1px solid rgba(106, 116, 137, 0.3);
    box-sizing: border-box;
    border-radius: 16px;
    outline: none;
  transition: all 0.2s;
}
</style>