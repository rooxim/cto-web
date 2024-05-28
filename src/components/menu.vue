<template>
  <div id="menu">
    <H1 class="title">dummy</H1>
    <table>
      <tr>
        <td>dummy</td>
        <td>dummy</td>
      </tr>
      <tr>
        <td>dummy</td>
        <td>dummy</td>
      </tr>
      <tr>
        <td>dummy</td>
        <td>dummy</td>
      </tr>
      <tr>
        <td>dummy</td>
        <td>dummy</td>
      </tr>
      <tr>
        <td>dummy</td>
        <td>dummy</td>
      </tr>
    </table>

    <div class="detail">
      <div class="item">
        <div>
          <picture>
            <source type="image/webp" srcset="@/assets/dummy.png?preset=img&format=webp&srcset">
            <img src="@/assets/dummy.png?preset=img&src" srcset="@/assets/dummy.png?preset=img&srcset" alt="dummy" />
          </picture>
        </div>
        <div class="itemTitle">dummy</div>
        <div class="description">
          dummy dummy dummy dummy dummy dummy dummy dummy dummy dummy dummy
        </div>
      </div>
      <div class="item">
        <div>
          <picture>
            <source type="image/webp" srcset="@/assets/dummy.png?preset=img&format=webp&srcset">
            <img src="@/assets/dummy.png?preset=img&src" srcset="@/assets/dummy.png?preset=img&srcset" alt="dummy"/>
          </picture>
        </div>
        <div class="itemTitle">dummy</div>
        <div class="description">
          dummy dummy dummy dummy dummy dummy dummy dummy dummy dummy dummy
        </div>
      </div>
      <div class="item">
        <div>
          <picture>
            <source type="image/webp" srcset="@/assets/dummy.png?preset=img&format=webp&srcset">
            <img src="@/assets/dummy.png?preset=img&src" srcset="@/assets/dummy.png?preset=img&srcset" alt="dummy"/>
          </picture>
        </div>
        <div class="itemTitle">dummy</div>
        <div class="description">
          dummy dummy dummy dummy dummy dummy dummy dummy dummy dummy dummy
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped lang="scss">
.detail{
  margin-top: 40px;
  display: flex;
  .item{
    padding: 5px;
    flex: 1;

    div{
      &:has(img){
        padding: 0;
        position: relative;
        &:after{
          position: absolute;
          content: '';
          top: 0;
          bottom: 0;
          left: 0;
          right: 0;
          box-shadow: inset 0 0 8px 8px white;
        }
      }
    }

    img{
      width: 100%;
    }
    .itemTitle{
      font-weight: bold;
      font-size: 24px;
    }
    .description{
      font-size: 20px;
    }
  }
}

#menu{
  padding: 0 20px;
  .title{
    text-align: center;
    font-size: 40px;
    font-weight: bold;
  }
  table{
    margin: 0 auto;
    font-size: 25px;
    border-collapse: collapse;
    font-weight: bold;
    tr{
      td:first-child{
        padding-top: 10px;
        width: 400px;
        border-bottom: solid 1px;
      }
      td:last-child{
        text-align: right;
        width: 100px;
        border-bottom: solid 1px;
        vertical-align: bottom;
      }
    }
  }
}

@media only screen and (max-width: 750px) {
  .detail{
    flex-direction: column;
    .item{
      padding: 20px 0;
    }
  }
  #menu{
    table{
      font-size: 19px;
    }
  }
}
</style>
<script setup lang="ts">
</script>
