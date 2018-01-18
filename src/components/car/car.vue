<template>
  <div class="bigbox">
      <!-- 顶部导航 -->
    <navheader></navheader>
    <!-- 购物车 -->
    <div class="carbox">
        <p class="allgoods">全部商品<span>1</span></p>
        <p class="list">
            <!-- `checked` 为 true 或 false -->
            <el-checkbox v-model="checked">全选</el-checkbox>
            <span class="goodname">商品名称</span>
            <span class="others">单价</span>
            <span class="others">数量</span>
            <span class="others">金额</span>
            <span class="others">操作</span>
        </p>
        <!-- 选择 -->
        <div class="detail">
           <div class="goodmes">
                <table>
                    <tr>
                        <td class="tdfist"><el-checkbox v-model="checked"></el-checkbox></td>
                        <td class="tdsec">
                        <img src="../../assets/images/comment/nai.png" alt="">
                        <div class="tdimg">
                            <p>a2 白金婴儿配方幼儿奶粉三段 900克/罐 4罐 1-3岁</p>
                            <p>不支持七天无理由退货</p>
                        </div> 
                        </td>
                        <td class="samel">
                        <p>$160</p>
                        <p>(会员价)</p>
                        </td>
                        <td class="samel">
                            <el-input-number size="small" v-model="num6"></el-input-number>
                        </td>
                        <td class="samel">
                            <p class="price">$160</p>
                            <p>4.52Kg</p>
                        </td>
                        <td class="samel">
                            <p>删除</p>
                            <p>移入我的收藏夹</p>
                        </td>
                    </tr>
                </table>
            </div>
        </div>
         <table class="all-de">
             <tr>
                 <td><el-checkbox v-model="checked"></el-checkbox></td>
                 <td></td>
             </tr>
         </table>
    </div>
     <!-- 底部介绍  -->
    <footlist></footlist>     
  </div>
</template>

<script>
export default {
    data() {
      return {
        checked: true,
         num6: 1,
      };
    },
    // methods: {
    //   handleChange(value) {
    //     console.log(value);
    //   }
    // },
  };
</script>

<style scoped>
    .carbox {
        width: 1200px;
        margin:0 auto;
        background-color: #fff;
        margin-top:20px;
        border:1px solid red;
    }
    .allgoods {
        font-size: 18px;
        height: 40px;
        line-height: 40px;
    }
    .allgoods span {
        color:#d4282d;
        margin-left:10px;
    }
    .carbox p {
        width:100%;
        
    }
    /*  全选 */
    .list {
        height: 50px;
        line-height: 50px;
       font-size:0; 
        background-color: #fafafa;
        margin-top:10px;
         padding-left:20px;
    }
    .list span {
        display:inline-block;
        font-size:14px;
    }
    .goodname {
        width:488px;
        text-align: center;
    }
    .others {
        width: 159px;
        text-align: center;
    }
    /* 选择 */
     .goodmes {
    background-color: #fdf4f4;
    margin-top:25px;
    margin-bottom: 40px;
    padding-left:20px;
  }
  td>img {
    float:left;
    width:90px;
    height:90px;
  }
  .tdimg {
    float:left;
    width:220px;
    margin-left:15px;
  }
  .tdimg p {
    height: 40px;
    line-height:20px;
  }
  .tdimg p:nth-child(2){
    color:#999;
  }

  .tdfist {
      width:40px;
  }
  .tdsec {
      width:500px;
  }
  tr {
    color:#333;
  }
  tr:first-child {
    height: 40px;
  }
  
  td {
    font-size: 14px;
    padding-top:15px;
    padding-bottom:15px;
  }
  .inter { 
    width:70px;
    height: 25px;
    line-height:25px;
    margin:0 auto;
    border-radius:5px;
    color:#d4282d; 
  }
  td p:nth-child(2) {
    margin-top:10px;
    color:#999;
  }
  .price {
    font-size:16px;            
  }
  .message {
      font-size:16px;
  }
  .samel {
      text-align: center;
  }

</style>

<style>
  .el-checkbox__input.is-checked .el-checkbox__inner, .el-checkbox__input.is-indeterminate .el-checkbox__inner {
    background-color: #d4282d;
    border-color: #d4282d;
}
.el-checkbox__input.is-focus .el-checkbox__inner {
    border-color: #d4282d;
}
.el-checkbox__inner:hover {
    border-color: #d4282d;
}
.el-checkbox__input.is-checked+.el-checkbox__label {
    color: #555;
}

</style>

