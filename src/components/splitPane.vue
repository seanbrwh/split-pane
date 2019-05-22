<template>
    <div :class="[split == 'vertical' ? 'vertical' : '',split=='horizontal'? 'horizontal': '']" >
        <pane  :class="[split == 'vertical' ? 'vertical-pane' : '',split=='horizontal'? 'horizontal-pane': '']">
            <slot name='pane1'></slot>
        </pane>
        <pane  :class="[split == 'vertical' ? 'vertical-pane' : '',split=='horizontal'? 'horizontal-pane': '']">
            <slot name='pane2'></slot>
        </pane>
    </div>
</template>

<script>
import pane from './pane'
export default {
    props:{
        split:String
    },
    components:{
        pane
    }
}
</script>

<style>
    .splitPane{
        width:100%;
        height: 100%;
    }   
    .vertical{
        display: flex;
        justify-content: space-evenly;
        flex-direction: row;
    }
    .vertical-pane{
        width:50%;
        height:80vh;
    }
    .horizontal-pane{
        height:40vh;
    }
    .horinzontal{
        display: flex;
        justify-content: space-evenly;
        flex-direction: column;
    }
</style>
