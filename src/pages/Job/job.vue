<template>
  <div class="w job-session">
    <el-container>
      <!-- 搜索栏 -->
      <el-header height="70px">
        <div class="search">
          <form action>
            <el-select
              v-model="value"
              multiple
              filterable
              remote
              reserve-keyword
              placeholder="请输入关键词"
              :remote-method="remoteMethod"
              :loading="loading"
            >
              <el-option
                v-for="item in options"
                :key="item.value"
                :label="item.label"
                :value="item.value"
              ></el-option>
            </el-select>
            <el-button
              type="info"
              icon="el-icon-search"
              size="medium"
              style="background-color:black"
            >搜索</el-button>
          </form>
        </div>
      </el-header>
      <el-main>
        <!-- 导航栏 -->
        <div class="job-info">
          <ul>
            <!-- 工作地点 -->
            <li class="job-place">
              <span>公司地点：</span>
              <span>
                <a href="javascript:;">全国</a>
              </span>
              <span>
                <a href="javascript:;">北京</a>
              </span>
              <span>
                <a href="javascript:;">上海</a>
              </span>
              <span>
                <a href="javascript:;">杭州</a>
              </span>
              <span>
                <a href="javascript:;">广州</a>
              </span>
              <span>
                <a href="javascript:;">深圳</a>
              </span>
              <span>
                <a href="javascript:;">南京</a>
              </span>
              <span>
                <a href="javascript:;">天津</a>
              </span>
              <span>
                <a href="javascript:;">重庆</a>
              </span>
              <span>
                <a href="javascript:;">长沙</a>
              </span>
              <el-popover placement="bottom" width="550" trigger="hover">
                <div class="more">
                  <p>ABCDEF</p>
                  <p>
                    <span>
                      <a href="javascript:;">北京</a>
                    </span>
                    <span>
                      <a href="javascript:;">长春</a>
                    </span>
                    <span>
                      <a href="javascript:;">成都</a>
                    </span>
                    <span>
                      <a href="javascript:;">重庆</a>
                    </span>
                    <span>
                      <a href="javascript:;">长沙</a>
                    </span>
                    <span>
                      <a href="javascript:;">常州</a>
                    </span>
                    <span>
                      <a href="javascript:;">东莞</a>
                    </span>
                    <span>
                      <a href="javascript:;">大连</a>
                    </span>
                    <span>
                      <a href="javascript:;">佛山</a>
                    </span>
                    <span>
                      <a href="javascript:;">福州</a>
                    </span>
                  </p>

                  <p>GHIJ</p>
                  <p>
                    <span>
                      <a href="javascript:;">贵阳</a>
                    </span>
                    <span>
                      <a href="javascript:;">广州</a>
                    </span>
                    <span>
                      <a href="javascript:;">哈尔滨</a>
                    </span>
                    <span>
                      <a href="javascript:;">合肥</a>
                    </span>
                    <span>
                      <a href="javascript:;">海口</a>
                    </span>
                    <span>
                      <a href="javascript:;">杭州</a>
                    </span>
                    <span>
                      <a href="javascript:;">惠州</a>
                    </span>
                    <span>
                      <a href="javascript:;">金华</a>
                    </span>
                    <span>
                      <a href="javascript:;">济南</a>
                    </span>
                    <span>
                      <a href="javascript:;">嘉兴</a>
                    </span>
                  </p>

                  <p>KLMN</p>
                  <p>
                    <span>
                      <a href="javascript:;">昆明</a>
                    </span>
                    <span>
                      <a href="javascript:;">廊坊</a>
                    </span>
                    <span>
                      <a href="javascript:;">宁波</a>
                    </span>
                    <span>
                      <a href="javascript:;">南昌</a>
                    </span>
                    <span>
                      <a href="javascript:;">南京</a>
                    </span>
                    <span>
                      <a href="javascript:;">南宁</a>
                    </span>
                    <span>
                      <a href="javascript:;">南通</a>
                    </span>
                  </p>

                  <p>OPQR</p>
                  <p>
                    <span>
                      <a href="javascript:;">青岛</a>
                    </span>
                    <span>
                      <a href="javascript:;">泉州</a>
                    </span>
                  </p>

                  <p>STUV</p>
                  <p>
                    <span>
                      <a href="javascript:;">上海</a>
                    </span>
                    <span>
                      <a href="javascript:;">石家庄</a>
                    </span>
                    <span>
                      <a href="javascript:;">绍兴</a>
                    </span>
                    <span>
                      <a href="javascript:;">沈阳</a>
                    </span>
                    <span>
                      <a href="javascript:;">深圳</a>
                    </span>
                    <span>
                      <a href="javascript:;">苏州</a>
                    </span>
                    <span>
                      <a href="javascript:;">天津</a>
                    </span>
                    <span>
                      <a href="javascript:;">太原</a>
                    </span>
                    <span>
                      <a href="javascript:;">台州</a>
                    </span>
                  </p>

                  <p>WXYZ</p>
                  <p>
                    <span>
                      <a href="javascript:;">武汉</a>
                    </span>
                    <span>
                      <a href="javascript:;">无锡</a>
                    </span>
                    <span>
                      <a href="javascript:;">温州</a>
                    </span>
                    <span>
                      <a href="javascript:;">西安</a>
                    </span>
                    <span>
                      <a href="javascript:;">厦门</a>
                    </span>
                    <span>
                      <a href="javascript:;">烟台</a>
                    </span>
                    <span>
                      <a href="javascript:;">珠海</a>
                    </span>
                    <span>
                      <a href="javascript:;">中山</a>
                    </span>
                    <span>
                      <a href="javascript:;">郑州</a>
                    </span>
                  </p>
                </div>
                <span></span>
                <span slot="reference">
                  <a href="javascript:;">其他</a>
                  <a href="javascript:;" class="triangle" @click="flag=ture"></a>
                </span>
              </el-popover>
            </li>
            <!-- 工作经验 -->
            <li>
              <span>工作经验：</span>
              <span>
                <a href="javascript:;">不限</a>
              </span>
              <span>
                <a href="javascript:;">实习生</a>
              </span>
              <span>
                <a href="javascript:;">应届毕业生</a>
              </span>
              <span>
                <a href="javascript:;">三年及以下</a>
              </span>
              <span>
                <a href="javascript:;">3-5年</a>
              </span>
              <span>
                <a href="javascript:;">5-10年</a>
              </span>
              <span>
                <a href="javascript:;">10年以上</a>
              </span>
            </li>
            <!-- 学历要求 -->
            <li>
              <span>学历要求：</span>
              <span>
                <a href="javascript:;">不限</a>
              </span>
              <span>
                <a href="javascript:;">高中及以下</a>
              </span>
              <span>
                <a href="javascript:;">大专</a>
              </span>
              <span>
                <a href="javascript:;">本科</a>
              </span>
              <span>
                <a href="javascript:;">硕士</a>
              </span>
              <span>
                <a href="javascript:;">博士</a>
              </span>
            </li>
            <!-- 融资阶段 -->
            <li>
              <span>融资阶段：</span>
              <span>
                <a href="javascript:;">不限</a>
              </span>
              <span>
                <a href="javascript:;">未融资</a>
              </span>
              <span>
                <a href="javascript:;">天使轮</a>
              </span>
              <span>
                <a href="javascript:;">A轮</a>
              </span>
              <span>
                <a href="javascript:;">B轮</a>
              </span>
              <span>
                <a href="javascript:;">C轮</a>
              </span>
              <span>
                <a href="javascript:;">D轮及以上</a>
              </span>
              <span>
                <a href="javascript:;">已上市</a>
              </span>
              <span>
                <a href="javascript:;">不需要融资</a>
              </span>
            </li>
            <!-- 公司规模 -->
            <li>
              <span>公司规模：</span>
              <span>
                <a href="javascript:;">不限</a>
              </span>
              <span>
                <a href="javascript:;">0-20人</a>
              </span>
              <span>
                <a href="javascript:;">20-99人</a>
              </span>
              <span>
                <a href="javascript:;">100-499人</a>
              </span>
              <span>
                <a href="javascript:;">500-999人</a>
              </span>
              <span>
                <a href="javascript:;">1000-9999人</a>
              </span>
              <span>
                <a href="javascript:;">10000以上</a>
              </span>
            </li>
          </ul>
        </div>
        <!-- 工作列表 -->
        <el-card class="job-card" shadow="always">
          <div v-for="j in jobbox" :key="j.id">
            <div class="j-card">
              <router-link to="/joblist">
                <div class="j-one">
                  <p class="j-f">
                    <span class="j-jobname">{{j.jobname}}</span>
                    <span class="j-salary">{{j.salary}}</span>
                  </p>
                  <p class="j-s">
                    <span>{{j.place}}</span>
                    <span>|</span>
                    <span>{{j.experience}}</span>
                    <span>|</span>
                    <span>{{j.academic}}</span>
                  </p>
                </div>
                <div class="j-two">
                  <p class="j-f">
                    <span>{{j.company}}</span>
                  </p>
                  <p class="j-s">
                    <span>{{j.stage}}</span>
                    <span>|</span>
                    <span>{{j.kind}}</span>
                  </p>
                </div>
                <div class="j-three">
                  <p class="j-f">
                    <span class="j-hr">{{j.hr}}</span>
                  </p>
                  <p class="j-s">
                    <span class="j-time">发布于：{{j.time}}</span>
                  </p>
                </div>
              </router-link>
            </div>
          </div>
        </el-card>
      </el-main>
      <el-footer class="page">
        <!-- 分页栏 -->
        <el-pagination background :page-size="20" layout="prev, pager, next" :total="1000"></el-pagination>
      </el-footer>
    </el-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      flag: false,
      options: [],
      value: [],
      list: [],
      loading: false,
      states: [
        "Alabama",
        "Alaska",
        "Arizona",
        "Arkansas",
        "California",
        "Colorado",
        "Connecticut",
        "Delaware"
      ],
      jobbox: [],
     
    };
  },
  created() {
    this.$axios.get('./static/data/job.json')
    .then(res => {
      this.jobbox = res.data.message
    })
    .catch(err => {
      console.log(err)
    })
  },

  mounted() {
    this.list = this.states.map(item => {
      return { value: `value:${item}`, label: `label:${item}` };
    });
  },
  methods: {
    remoteMethod(query) {
      if (query !== "") {
        this.loading = true;
        setTimeout(() => {
          this.loading = false;
          this.options = this.list.filter(item => {
            return item.label.toLowerCase().indexOf(query.toLowerCase()) > -1;
          });
        }, 200);
      } else {
        this.options = [];
      }
    }
  }
};
</script>

<style>
.job-session {
  position: relative;
}
.job-info {
  background-color: #fafafa;
  padding: 10px 10px 10px 20px;
}
.job-info ul li {
  margin: 20px 14px;
}
.job-palce {
  position: absolute;
}
.job-info span {
  margin: 0 7px;
}
/* 下拉地区 */ 
.more p{
  margin: 7px;
}
.more p span {
  margin: 0 7px;
  font-size: 16px;
  color: #333;
}
/* 搜索栏 */
.search {
  height: 60px;
  width: 820px;
  /* position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%); */
  margin: 5px auto;
  line-height: 60px;
}
.el-select {
  width: 700px;
}
.job-card {
  position: relative;
  height: 820px;
  overflow: hidden;
  padding-bottom: 20px;
  display: inline-block;
  background-color: #fafafa9f;
}
.j-card {
  width: 1100px;
  height: 80px;
  margin: 7px 7px;
  padding: 5px 20px;
  box-sizing: border-box;
  line-height: 80px;
  border-radius: 2px;
  box-shadow: 2px 2px 2px #d8d5d5;
  border: 1px dotted #c9c6c6ef;
  background-color: #fafafa77;
}
.j-one,
.j-two,
.j-three {
  float: left;
  height: 70px;
  color: #61687c;
}
.j-one {
  width: 340px;
  margin: 0 10px 0 0;
}
.j-two {
  width: 340px;
  margin: 0 40px;
}
.j-three {
  width: 270px;
  margin: 0 7px;
}
.j-f {
  position: absolute;
  height: 40px;
  font-weight: 400;
  font-size: 18px;
  box-sizing: border-box;
}
.j-f span {
  position: absolute;
  float: left;
  height: 40px;
  line-height: 40px;
  top: 0;
}
.j-s {
  height: 30px;
}
.j-s span {
  height: 30px;
  float: left;
  line-height: 30px;
  margin: 0 5px;
  top: 0;
}
.j-one p,
.j-two p {
  position: relative;
  width: 350px;
}
.j-three p {
  position: relative;
  width: 270px;
}
.j-jobname {
  color: black;
}
.j-salary {
  right: 10px;
  color: red;
}
.j-hr,
.j-time {
  position: absolute;
  font-size: 16px;
  color: #8d92a1;
  right: 10px;
}
.j-hr {
  color: black;
}
</style>