<template>
    <div class="top">
        <div class="top__header">
            <div class="iconfont top__header__back" @click="handleBack">&#xe677;</div>
            确认订单
        </div>
        <div class="top__receiver">
            <div class="top__receiver__title">收货地址</div>
            <div class="top__receiver__address">天津理工大学8号学生公寓325室</div>
            <div class="top__receiver__info">
                <span class="top__receiver__info__name">赵子明</span>
                <span class="top__receiver__info__name">18551554851</span>
            </div>
            <div class="top__receiver__icon iconfont">&#xe677;</div>
        </div>
    </div>
</template>
<script>
import { useRouter } from 'vue-router'
export default {
  name: 'Top',
  setup () {
    const router = useRouter()
    const handleBack = () => {
      router.back()
    }
    return { handleBack }
  }
}
</script>,
<style lang="scss" scoped>
.top{
    position: relative;
    width: 100%;
    height: 1.96rem;
    background-size: 100% 1.59rem;
    background-image: linear-gradient(0deg, rgba(0,145,255,0.00) 4%, #0091ff 50%);
    background-repeat: no-repeat;
    &__header{
        padding-top: .2rem;
        line-height: .24rem;
        color: #fff;
        text-align: center;
        position: relative;
        font-size: .16rem;
        &__back{
            position: absolute;
            left: .18rem;
        }
    }
    &__receiver{
        position: absolute;
        left: .18rem;
        right: .18rem;
        bottom: 0;
        height: 1.11rem;
        background-color: #fff;
        border-radius: .04rem;
        &__title{
            padding: .16rem 0 .14rem .16rem;
            font-size: .16rem;
            color: #333;
            line-height: .22rem;
        }
        &__address{
            padding: 0 .4rem 0 .16rem;
            font-size: .14rem;
            color: #333;
            line-height: .2rem;
        }
        &__info{
            padding: .06rem 0 0 .16rem;
            &__name{
                color: #666;
                font-size: .12rem;
                line-height: .18rem;
                margin-right: .16rem;
            }
        }
        &__icon{
            position: absolute;
            right: .2rem;
            top: .5rem;
            color: #666;
            font-size: .16rem;
            transform: rotate(180deg);
        }
    }
}
</style>
