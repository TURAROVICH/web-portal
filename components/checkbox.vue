<template>
    <div class="checkbox-container">
        <div @click="is=!is" class="checkbox">
            <svg v-if="is" width="17" height="15" viewBox="0 0 13 10" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path fill-rule="evenodd" clip-rule="evenodd" d="M12.7576 0.180429C13.0557 0.442514 13.0826 0.893993 12.8176 1.18884L5.11387 9.76026C4.97682 9.91275 4.78037 10 4.57408 10C4.36778 10 4.17134 9.91275 4.03428 9.76026L0.182434 5.47455C-0.0825619 5.1797 -0.0557092 4.72822 0.242411 4.46614C0.540532 4.20406 0.997028 4.23061 1.26202 4.52546L4.57408 8.21057L11.738 0.239748C12.003 -0.0550971 12.4595 -0.0816547 12.7576 0.180429Z" fill="#2CC84D"/>
            </svg>
        </div>
        <div class="desc" v-html="desc"></div>
    </div>
</template>


<script>
export default {
    props:['desc'],
    data:()=>({
        is:false
    })
}
</script>

<style lang="scss" scoped>
.checkbox-container{
    display: flex;
    align-items: center;
    gap:10px;
    .checkbox{
    border: 1px solid rgba(106, 116, 137, 0.3);
    box-sizing: border-box;
    border-radius: 4px;
    width: 24px;
    height: 24px;
    display: flex;
    align-items: center;
    justify-content: center;
    }
    .desc   {
            /* Body/Regular */

    font-family: Nunito;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 24px;
    /* identical to box height, or 150% */

    display: flex;
    align-items: center;

    /* Text/Primary */

    color: #252A36;
    }
}
</style>