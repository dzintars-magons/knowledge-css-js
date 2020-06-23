<template>

            <div class="box-container">
                 <div class="boxes row">
                    <div class="box-1 col-12 col-md-4"></div>
                    <div class="box-2 col-12 col-md-4"></div>
                    <div class="box-3 col-12 col-md-4"></div>
                </div>

                <div class="horizontal-boxes">
                    <div class="box-1"></div>
                    <div class="box-2"></div>
                    <div class="box-3"></div>
                    <div class="box-4"></div>
                </div>

            </div>

       
   
</template>

<script>
export default {
    
}
</script>

<style lang="scss">

    .box-container {
        @include container;
    }

    .boxes {

        margin-top: 25px;
        
    }

    .box-1, .box-2, .box-3 {

        height: 300px;
        width: 300px;
       

    }

    // .box-1, .box-2 {
    //     margin-right: 25px;
    // }



    .box-1 {
        background: firebrick;
        //better write in ms because javascript understands ms
        //usually animations range from 250ms to 500ms , and 1000ms would be too slow
        transition-duration: 500ms;
        //it is advised to specify those properties that are affected by the transition to normalize CPU loads
        transition-property: background-color, transform;
        transition-timing-function: ease;
            &:hover {
                    background-color: gold;
                    transform: rotate(45deg);
                }
    }

    .box-2 {
        background: purple;
    }

    .box-3 {
        background: teal;
    }
  

    .box {
        margin-top: 250px;
        margin-left: 250px;
        
        width: 300px;
        height: 300px;
        background: purple;
        
            &:hover {
                background: firebrick;
            }
    }



</style>