<template>
    <div class="modal-container" >
        <div class="modal">
            <div class="close">
                <svg  @click="$emit('close')" width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
                <rect width="32" height="32" rx="10" fill="#6A7489" fill-opacity="0.3"/>
                <path d="M20 8L12 16L20 24" stroke="white" stroke-width="2" stroke-linecap="round"/>
                </svg>
                <div class="close-title">Подробнее</div>

            </div>

            <div class="body">
                <div class="profile">
                    <img width="128" height="128" src="@/assets/imgs/test/profile.png" alt="">
                    <div class="title">MAG Interactive</div>
                </div>

                <div class="grid-inputs-cnt">
                    <div class="form">
                        <div class="form-title">О компании</div>
                        <div class="inputs">
                            <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='name' required />
                            <label for="name" class="form__label">Юридический адрес</label>
                            </div>
                            <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='name' required />
                            <label for="name" class="form__label">Фактический адрес</label>
                            </div>
                            <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='name' required />
                            <label for="name" class="form__label">ФИО руководителя</label>
                            </div>
                            <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='name' required />
                            <label for="name" class="form__label">Должность руководителя</label>
                            </div>
                            <div style="margin-top:18px;" class="form-title">Контакты</div>
                             <masked-input
                                type="text"
                                name="phone"
                                class="form-control"
                                v-model="phone"
                                :mask="['(', /[1-9]/, /\d/, /\d/, ')', ' ', /\d/, /\d/, /\d/, '-', /\d/, /\d/, /\d/, /\d/]"
                                :guide="false"
                                placeholder="Телефон">
                                </masked-input>
                            <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='name' required />
                            <label for="name" class="form__label">Email</label>
                            </div>
                        </div>
                    </div>
                    <div class="form">
                        <div class="form-title">Реквизиты</div>
                        <div class="inputs">
                            <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='name' required />
                            <label for="name" class="form__label">ИНН</label>
                            </div>
                            <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='name' required />
                            <label for="name" class="form__label">КПП</label>
                            </div>
                            <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='name' required />
                            <label for="name" class="form__label">КПП</label>
                            </div>
                            <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='name' required />
                            <label for="name" class="form__label">Расчетный счет</label>
                            </div>
                            <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='name' required />
                            <label for="name" class="form__label">Корреспондентский счет</label>
                            </div>
                            <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='name' required />
                            <label for="name" class="form__label">БИК</label>
                            </div>
                            <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='name' required />
                            <label for="name" class="form__label">Наименование банка</label>
                            </div>

                        </div>
                    </div>
                </div>
                <div class="btns">
                    <div class="btn-1">
                        <span>Заблокировать</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>


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
            .btns{
                display: flex;
                align-items: center;
                gap: 32px;
                .btn-1{
                    display: flex;
                    flex-direction: row;
                    justify-content: center;
                    align-items: center;
                    padding: 16px 28px;

                    position: static;
                    width: 272px;
                    height: 56px;
                    left: 0px;
                    top: 0px;

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
                .btn-2{
                    display: flex;
                    flex-direction: row;
                    justify-content: center;
                    align-items: center;
                    padding: 16px 28px;

                    position: static;
                    width: 272px;
                    height: 56px;
                    left: 304px;
                    top: 0px;

                    /* BG/Primary */

                    background: #FFFFFF;
                    /* Accent/Primary */

                    border: 1px solid #2CC84D;
                    box-sizing: border-box;
                    border-radius: 16px;
                    span{
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
                }
            }
            .grid-inputs-cnt{
                display: grid;
                grid-template-columns: 1fr 1fr;
                grid-column-gap: 48px;
                margin: 48px 0;
                .inputs{
                    display: flex;
                    flex-direction: column;
                    gap: 32px;
                    margin-top: 32px;

                }
                .form{
                    .form-title{
                        /* H6/Bold */
                        border-bottom:1px solid #F1F3F8;
                        padding: 8px;
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
            }
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
      width:100%;
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