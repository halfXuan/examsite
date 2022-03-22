<template>
    <div class="header">
        <div class="content">
            <div class="navs">
                <div class="title">
                    湖北省2022年广播体操新套路培训
                </div>
                <el-menu :default-active="activeIndex" class="elDemo" mode="horizontal" @select="handleSelect">
                    <el-menu-item index="1">课程列表</el-menu-item>
                    <el-menu-item index="2">考试</el-menu-item>
                    <el-menu-item index="3">打卡记录</el-menu-item>
                    <el-menu-item index="4">个人中心</el-menu-item>
                    <el-menu-item index="5" @mouseover.native="handleApp">手机端观看</el-menu-item>
                </el-menu>
            </div>
            <el-link type='primary' class="login" :underline="false">登录</el-link>
        </div>
        <div class="footer">
            <el-row>
                <el-col :span='6' :class="activeIndex==1?'actived':''" @click.native="handleMenu('1')">
                    <i class="icon iconfont icon-home"></i>
                    <p>课程列表</p>
                </el-col>
                <el-col :span='6'  :class="activeIndex==2?'actived':''" @click.native="handleMenu('2')">
                    <i class="icon iconfont icon-exam"></i>
                    <p>考试</p>
                </el-col>
                <el-col :span='6' :class="activeIndex==3?'actived':''" @click.native="handleMenu('3')">
                    <i class="icon iconfont icon-record"></i>
                    <p>打卡记录</p>
                </el-col>
                <el-col :span='6' :class="activeIndex==4?'actived':''" @click.native="handleMenu('4')">
                    <i class="icon iconfont icon-mine"></i>
                    <p>个人中心</p>
                </el-col>
            </el-row>
        </div>
    </div>
</template>
<script>
export default {
  name: 'Header',
  data () {
    return {
      activeIndex: '1'
    }
  },
  methods: {
    handleSelect () {
      console.log(1)
    },
    handleApp () {
      console.log(2)
    },
    handleMenu (index) {
      this.activeIndex = index
    }
  }
}
</script>
<style lang="less" scoped>

.header{
    width: 100%;
    background-color: #fff;
    position: fixed;
    left: 0;
    top: 0;
    right: 0;
    height: 64px;
    box-shadow: 0 1px 2px 0 rgb(0 0 0 / 5%);
    .content{
        width: 1200px;
        margin: 0 auto;
        height: 64px;
        color: #666;
        font-size: 16px;
        text-align: center;
        display: flex;
        justify-content: space-between;
        .navs{
            display: flex;
            justify-content: space-between;
            .title{
                line-height: 64px;
                font-size: 18px;
            }
            .elDemo{
                margin-left: 150px;
            }
        }
    }
}
.footer{
    display: none;
    position: fixed;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: #fff;
    height: 50px;
    .el-col{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        line-height: 20px;
        padding-top: 5px;
        color: #999;
        i{
            font-size: 18px!important;
        }
        p{
            font-size: 14px!important;
        }
    }
    .actived{
        color: #409eff;
    }
}
@media screen and (max-width: 1200px) {
    .header{
        .content{
            width: 100%!important;
            padding:0 20px;
             .navs{
                 .title{
                    font-size: 16px;
                }
                .elDemo{
                    margin-left: 50px!important;
                }
             }
        }
    }
}
@media screen and (max-width: 850px) {
    .header{
        height: 44px;
        .content{
            width: 100%!important;
            padding:0 20px;
            justify-content: center;
            height: 44px;
            .navs{
                justify-content: center;
                .title{
                    line-height: 44px;
                }
            }
            .elDemo{
                display: none;
            }
            .login{
                display: none;
            }
        }
    }
    .footer{
        display: block;
    }
}
.el-menu.el-menu--horizontal{
    border-bottom: none;
}
</style>
