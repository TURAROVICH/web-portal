<template>
    <div class="modal-container" >
        <div class="modal">
            <div class="close">
                <svg  @click="$emit('close')" width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
                <rect width="32" height="32" rx="10" fill="#6A7489" fill-opacity="0.3"/>
                <path d="M20 8L12 16L20 24" stroke="white" stroke-width="2" stroke-linecap="round"/>
                </svg>
                <h3 class="close-title">Подробнее</h3>

            </div>

            <div class="body">
                <div class="profile">
                    <img width="128" height="128" src="@/assets/imgs/test/profile.png" alt="">
                    <h1 class="title">Камила Ковалёва</h1>
                    <div class="is-online">
                    </div>
                </div>

                <div class="grid-inputs-cnt">
                    <div class="form">
                        <h4 class="form-title">О себе</h4>
                        <div class="inputs">
                            <div class="info">
                                Публичная информация
                            </div>
                            <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='name' required />
                            <label for="name" class="form__label">Сайт / Ссылка на соцсети</label>
                            </div>
                             <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='name' required />
                            <label for="name" class="form__label">Никнейм</label>
                            </div>
                            <textarea id="about-me" placeholder="Обо мне" cols="30" rows="10"></textarea>
                            <div class="info">Личная информация</div>
                            <masked-input
                                type="text"
                                name="phone"
                                class="form-control"
                                :mask="['+',7,'(', /[1-9]/, /\d/, /\d/, ')', ' ', /\d/, /\d/, /\d/, '-', /\d/, /\d/, /\d/, /\d/]"
                                :guide="false"
                                placeholder="Номер телефона">
                                </masked-input>
                             <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='email' required />
                            <label for="email" class="form__label">Email</label>
                            </div>
                             <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='mail' required />
                            <label for="mail" class="form__label">Адресс для корреспонденции</label>
                            </div>
                        </div>
                    </div>
                    <div class="form">
                        <h4 class="form-title">Паспортные данные</h4>
                        <div class="inputs">
                            <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='fio' required />
                            <label for="fio" class="form__label">ФИО</label>
                            </div>
                            <div class="flex gap-2">
                               <masked-input
                                type="text"
                                name="phone"
                                class="form-control"
                                :mask="[ /\d/, /\d/, /\d/, /\d/]"
                                :guide="false"
                                placeholder="Серия">
                                </masked-input>
                            <masked-input
                                type="text"
                                name="phone"
                                class="form-control"
                                :mask="[ /\d/, /\d/, /\d/, /\d/, /\d/, /\d/]"
                                :guide="false"
                                placeholder="Номер">
                                </masked-input>
                            </div>
                             <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='who' required />
                            <label for="who" class="form__label">Кем выдан</label>
                            </div>

                             <div class="flex gap-2">
                                <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='when' required />
                            <label for="when" class="form__label">Когда</label>
                            </div>
                            <div class="form__group field">
                            <input type="input" class="form__field" placeholder="Name" name="name" id='birth' required />
                            <label for="birth" class="form__label">Дата рождения</label>
                            </div>
                            </div>

                            <h4 class="form-title">Сканы документов</h4>
                            <div class="info">
                               Скан розового билета
                            </div>
                            <a href="https://osc.gov/Shared%20Documents/Set%20Adobe%20as%20the%20defualt%20PDF%20program.pdf" class="flex gap-4 items-center cursor-pointer">
                                
                                <svg width="18" height="22" viewBox="0 0 18 22" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M17.0297 5.76641L11.9859 0.720313C11.8453 0.579688 11.6531 0.5 11.4539 0.5H1.5C1.08516 0.5 0.75 0.835156 0.75 1.25V20.75C0.75 21.1648 1.08516 21.5 1.5 21.5H16.5C16.9148 21.5 17.25 21.1648 17.25 20.75V6.29609C17.25 6.09687 17.1703 5.90703 17.0297 5.76641ZM6.375 8.42188C6.89297 8.42188 7.3125 8.84141 7.3125 9.35938C7.3125 9.87734 6.89297 10.2969 6.375 10.2969C5.85703 10.2969 5.4375 9.87734 5.4375 9.35938C5.4375 8.84141 5.85703 8.42188 6.375 8.42188ZM13.3125 15.3125H4.6875C4.53047 15.3125 4.44375 15.132 4.53984 15.0102L6.87891 12.0289C6.89645 12.0065 6.91886 11.9884 6.94444 11.9759C6.97002 11.9634 6.9981 11.957 7.02656 11.957C7.05502 11.957 7.0831 11.9634 7.10869 11.9759C7.13427 11.9884 7.15668 12.0065 7.17422 12.0289L8.1375 13.257L9.96094 10.932C9.97848 10.9096 10.0009 10.8915 10.0265 10.879C10.0521 10.8666 10.0801 10.8601 10.1086 10.8601C10.1371 10.8601 10.1651 10.8666 10.1907 10.879C10.2163 10.8915 10.2387 10.9096 10.2562 10.932L13.4555 15.0102C13.5562 15.132 13.4672 15.3125 13.3125 15.3125ZM11.1094 6.64062V2.22969L15.5203 6.64062H11.1094Z" fill="black"/>
                                </svg>
                                <strong>document_file_picture.png</strong>
                            </a>


                            <div class="info">
                              Скан паспорта
                            </div>
                            <a href="https://osc.gov/Shared%20Documents/Set%20Adobe%20as%20the%20defualt%20PDF%20program.pdf" class="flex gap-4 items-center cursor-pointer">
                                <svg width="18" height="22" viewBox="0 0 18 22" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M17.0297 5.76641L11.9859 0.720313C11.8453 0.579688 11.6531 0.5 11.4539 0.5H1.5C1.08516 0.5 0.75 0.835156 0.75 1.25V20.75C0.75 21.1648 1.08516 21.5 1.5 21.5H16.5C16.9148 21.5 17.25 21.1648 17.25 20.75V6.29609C17.25 6.09687 17.1703 5.90703 17.0297 5.76641ZM6.375 8.42188C6.89297 8.42188 7.3125 8.84141 7.3125 9.35938C7.3125 9.87734 6.89297 10.2969 6.375 10.2969C5.85703 10.2969 5.4375 9.87734 5.4375 9.35938C5.4375 8.84141 5.85703 8.42188 6.375 8.42188ZM13.3125 15.3125H4.6875C4.53047 15.3125 4.44375 15.132 4.53984 15.0102L6.87891 12.0289C6.89645 12.0065 6.91886 11.9884 6.94444 11.9759C6.97002 11.9634 6.9981 11.957 7.02656 11.957C7.05502 11.957 7.0831 11.9634 7.10869 11.9759C7.13427 11.9884 7.15668 12.0065 7.17422 12.0289L8.1375 13.257L9.96094 10.932C9.97848 10.9096 10.0009 10.8915 10.0265 10.879C10.0521 10.8666 10.0801 10.8601 10.1086 10.8601C10.1371 10.8601 10.1651 10.8666 10.1907 10.879C10.2163 10.8915 10.2387 10.9096 10.2562 10.932L13.4555 15.0102C13.5562 15.132 13.4672 15.3125 13.3125 15.3125ZM11.1094 6.64062V2.22969L15.5203 6.64062H11.1094Z" fill="black"/>
                                </svg>
                                <strong>document_file_picture.png</strong>
                            </a>


                        </div>
                    </div>
                </div>
                <div class="btns">
                    <button class="btn-1">
                        <span>Зарегистрировать</span>
                    </button>
                    <button class="btn-2">
                        <span>Отправить на доработку</span>
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
#about-me{
    width: 360px;
    height: 139.99px;
    /* BG/Primary */

    background: #FFFFFF;
    /* Text/Tertiary */

    border: 1px solid rgba(106, 116, 137, 0.3);
    box-sizing: border-box;
    border-radius: 16px;
    outline: none;
    padding: 16px;
}
.info{
    /* Subheadline/Bold */

font-family: Nunito;
font-style: normal;
font-weight: bold;
font-size: 18px;
line-height: 24px;
/* identical to box height, or 133% */


/* Text/Secondary */

color: rgba(106, 116, 137, 0.5);

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
                position: relative;
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