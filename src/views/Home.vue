<template>
  <div class="home">
    <y-loading v-if="loading">
      <div class="loading-text">数据加载中...</div>
    </y-loading>
    <y-container :options="{width: 3840, height: 2160}">
      <div class="header">
        <top-header></top-header>
      </div>
      <div class="separator"></div>
      <div class="center">
        <div class="left">
          <div class="left1">{{k}}
          <button @click="add">di</button>
          </div>
          <div class="left2">2</div>
          <div class="left3">3</div>
          <div class="left4">4</div>
          <div class="left5">5</div>
          <div class="left6">6</div>
        </div>
        <div class="right">
          <div class="right-top1">1</div>
          <div class="right-top2">2</div>
          <div class="right-bottom">
            <div class="right-left">
              <div class="right-left1">1</div>
              <div class="right-left2">2</div>
              <div class="right-left3">3</div>
              <div class="right-left4">4</div>
            </div>
            <div class="right-right">
              <div class="right-right1">1</div>
              <div class="right-right2">2</div>
            </div>
          </div>
        </div>
      </div>
    </y-container>
  </div>
</template>

<script>
  import { ref, onMounted } from 'vue'
  import TopHeader from '@/components/TopHeader'

  export default {
    name: 'Home',
    components: {
      TopHeader
    },
    setup () {
      const k = ref({ a: 1, b: 2 })

      const loading = ref(true)
      onMounted(() => {
        setTimeout(_ => {
          loading.value = false
        }, 100)
      })

      const add = () => {
          k.value.a = 'ee'
      }
      return {
        loading,
        k,
        add
      }
    }
  }
</script>

<style lang="scss">
  .home {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
    background: rgb(29, 29, 29);
    color: #fff;
    font-size: 48px;
    #y-container{
      /*使用flex布局后，指定宽高*/
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      width: 100%;
      height: 100%;
      .header{
        width: 100%;
        height: 167px;
        background: yellowgreen;
      }
      .separator{
        width: 100%;
        height: 10px;
        background: rgba(92,88,89);
      }
      .center{
        width: 100%;
        flex: 1;
        display: flex;
        background: #42b983;
        .left{
          flex:0 0 860px;
          display: flex;
          flex-direction: column;
          justify-content: space-between;
          width: 860px;
          height: 100%;
          padding-bottom: 20px;
          box-sizing: border-box;
          background: red;
          .left1{
            height: 300px;
            background: yellowgreen;
          }
          .left2{
            height: 320px;
            background: #2c3e50;
          }
          .left3{
            height: 280px;
            background: greenyellow;
          }
          .left4{
            height: 230px;
            background: gold;
          }
          .left5{
            height: 360px;
            background: fuchsia;
          }
          .left6{
            height: 360px;
            background: forestgreen;
          }
        }
        .right{
          flex: 1;
          display: flex;
          flex-direction: column;
          background: orange;
          .right-top1{
            width: 100%;
            height: 206px;
            background: darkmagenta;
          }
          .right-top2{
            width: 100%;
            height: 48px;
            background: green;
          }
          .right-bottom{
            flex: 1;
            display: flex;
            padding-bottom: 20px;
            background: rebeccapurple;
            .right-left{
              flex: 0 0 1917px;
              display: flex;
              justify-content: space-between;
              flex-direction: column;
              width: 1917px;
              .right-left1{
                background: darkorange;
                height: 999px;
              }
              .right-left2{
                height: 80px;
                background: aqua;
              }
              .right-left3{
                height: 350px;
                background: blue;
              }
              .right-left4{
                height: 220px;
                background: red;
              }
            }

            .right-right{
              flex: 1;
              display: flex;
              flex-direction: column;
              justify-content: space-between;
              margin-left: 10px;
              .right-right1{
                width: 100%;
                height: 999px;
                background: olivedrab;
              }
              .right-right2{
                margin-top: 20px;
                width: 100%;
                flex: 1;
                background: #42b983;
              }
            }
          }
        }
      }

      .loading-text {
        font-size: 20px;
        margin-top: 10px;
      }
    }

  }
</style>
