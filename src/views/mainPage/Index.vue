<template>
  <div class="root" ref="root">
    <!-- 导航栏部分 -->
    <Nav :activateNum="activateNum"></Nav>
    <!-- 中间部分 -->
      <Row class="main">
        <!-- 博文部分 -->
        <Col span="22" offset="1" :xl="{span: 13, offset: 2}" :lg="{span: 14, offset: 2}"  style="height: 100%; margin-top: 25px;">
          <Essay></Essay>
        </Col>
        <!-- 数据部分 -->
        <Col span="22" offset="1" :xl="{span: 7, offset: 1}" :lg="{span: 6, offset: 1}"  style="height: 100%;margin-top: 25px;">
           <Palette></Palette>
        </Col>
      </Row>
      <Row style="margin-bottom: 5px;">
          <Col span="22" offset="1"  :xl="{span: 21, offset: 2}"   class="beian-block">
            <Button type="text" to="//beian.miit.gov.cn/?spm=5176.13841030.7y9jhqsfz.109.5fb45c69CIAYaF" target="_blank">赣ICP备19010015号</Button>
          </Col>
      </Row>
  </div>
</template>

<script>
import Nav from '../../components/nav/Nav'
import Palette from '../../components/content/Palette'
import Essay from '../../components/content/Essay'
export default {
  name: 'Index',
  components: {
    Nav,
    Palette,
    Essay
  },
  data () {
    return {
      activateNum: 0,
      imgUrl: '../../../static/imgs/avlt.png'
    }
  },
  methods: {}
}
</script>

<style lang="less" scoped>
  .root {
    width: 100%;
    height: 100%;
    position: relative;
  }
  .main {
    height: auto;
    padding-bottom: 50px;
    z-index: 29;
  }
  .beian-block {
    height: 50px;
    line-height: 50px;
    border-radius: 5px;
    margin-bottom: 5px;
    text-align: center;
    color: #000;
    background-color: #fff;
  }
</style>
