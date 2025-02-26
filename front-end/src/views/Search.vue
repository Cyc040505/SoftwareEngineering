<script>
import Head2 from "@/components/Head2.vue";
import {watch} from "vue";
import {useRoute} from "vue-router";

export default {
  name: "Search",
  components: {
    Head2
  },
  setup() {
    const $route = useRoute()
    watch(() => $route.query, () => {
      const searchbox = $route.query.q.toUpperCase();
      const storeitems = document.getElementById("product-list")
      if (storeitems) {
        const product = document.querySelectorAll(".product")
        const pname = storeitems.getElementsByTagName("p")

        for (var i = 0; i < pname.length; i++) {
          let match = product[i].getElementsByTagName('p')[0];

          if (match) {
            let textvalue = match.textContent || match.innerHTML

            if (textvalue.toUpperCase().indexOf(searchbox) > -1) {
              product[i].style.display = "";
            } else {
              product[i].style.display = "none";
            }
          }
        }
      }
    })
  }
}
</script>


<template>
  <Head2/>
  <div>
    <div class="searchbox">
      <div class="product-list" id="product-list">
        <div class="l">
          <strong>考试项目</strong>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">普通高考</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">成人高考</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">研究生考试</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">教师资格证考试</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">同等学力申请硕士学位考试</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">全国大学英语四、六级考试(CET)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">全国计算机等级考试(NCRE)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">全国计算机应用水平考试(NIT)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">全国英语等级考试(PETS)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">全国外语水平考试(WSK)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">全国外语水平考试(WSK)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank"> 书画等级考试(CCPT)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">中国少数民族汉语水平等级考试(MHK)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">托福网考®(TOEFL iBT®)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">雅思(IELTS)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">德福(TestDaF)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">日本语能力测试(JLPT)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">韩国语能力考试 (TOPIK)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">美国研究生入学考试(GRE)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">美国管理学研究生入学考试(GMAT)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">剑桥商务英语证书考试 (BEC)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">法语(DELF-DALF)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">对外西班牙语水平证书考试(DEL)E</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">美国法学院入学考试 (LSAT)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">巴西葡萄牙语(GELPE-BRAS)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">剑桥少儿英语 (CYLE)</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#" target="_blank">国家外语能力测评体系</a></p>
            </div>
          </div>
          <span>没有更多了...</span>
        </div>
        <div class="r">
          <strong>备考方案</strong>
          <div class="product">
            <div class="p-details">
              <p><a href="#">CET备考方案1</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#">CET备考方案2</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#">CET备考方案3</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#">CET备考方案4</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#">PET备考方案1</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#">PET备考方案2</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#">PET备考方案3</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#">PET备考方案4</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#">IELTS备考方案1</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#">IELTS备考方案2</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#">IELTS备考方案3</a></p>
            </div>
          </div>
          <div class="product">
            <div class="p-details">
              <p><a href="#">IELTS备考方案4</a></p>
            </div>
          </div>
          <span>没有更多了...</span>
        </div>

      </div>
    </div>
  </div>
</template>

<style scoped>
@import "../assets/css/Search.css";
</style>