<template>
  <v-app id="inspire">
    <v-main>
      <v-container class="py-8 px-6" fluid>
        <v-row>
          <v-col cols="12">
            <v-card>
              <v-toolbar color="pink" dark dense flat>
                <v-toolbar-title class="body-2">
                  stop10
                </v-toolbar-title>
              </v-toolbar>
              <v-list two-line>
                <template v-for="(item, index) in tenBooks">
                  <v-list-item :key="item.title" @click="goFeel(item.feel)">
                    <v-list-item-avatar color="red lighten-1">
                      <span class="white--text headline">{{item.times}}</span>
                    </v-list-item-avatar>
                    <v-list-item-content>
                      <v-list-item-title>{{item.title}}</v-list-item-title>
                      <v-list-item-subtitle>{{item.author}}</v-list-item-subtitle>
                    </v-list-item-content>
                  </v-list-item>
                  <v-divider v-if="index !== 9" :key="`divider-${index}`" inset></v-divider>
                </template>
              </v-list>
            </v-card>
          </v-col>
          <v-col cols="12">
            <v-card>
              <v-subheader>other</v-subheader>
              <v-list two-line>
                <template v-for="(item, index) in otherBooks">
                  <v-list-item :key="item.title">
                    <v-list-item-avatar color="grey darken-1">
                      <span class="white--text headline">{{item.times}}</span>
                    </v-list-item-avatar>
                    <v-list-item-content>
                      <v-list-item-title>{{item.title}}</v-list-item-title>
                      <v-list-item-subtitle>{{item.author}}</v-list-item-subtitle>
                    </v-list-item-content>
                  </v-list-item>
                  <v-divider v-if="index !== otherBooks.length -1 " :key="`divider-${index}`" inset></v-divider>
                </template>
              </v-list>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    cards: ["top10", "other"],
    books: [
      {
        title: "《财富自由之路》",
        author: "李笑来",
        times: "3",
        feel: ["升级概念"]
      },
      {
        title: "《让时间陪你慢慢变富》",
        author: "李笑来",
        times: "1",
        feel: ["定投的奥德修斯"]
      },
      {
        title: "《富爸爸穷爸爸》",
        author: "罗伯特·清崎",
        times: "1",
        feel: ["财商入门"]
      },
      {
        title: "《当谈跑步时，我谈些什么》",
        author: "春上村树",
        times: "1",
        feel: ["一个矮个子的真实"]
      },
      {
        title: "《人类简史》",
        author: "尤瓦尔·赫拉利",
        times: "1",
        feel: [
          "鬼才简话人类",
          "压力会越来越大，享受现代的压力，免受时代之苦，方得幸福"
        ]
      },
      {
        title: "《反脆弱》",
        author: "纳西姆·尼古拉斯·塔勒布",
        times: "1",
        feel: [
          "肌肉男的实干家",
          "杠铃模式反脆弱，野蛮生长",
          "把行李自然给了侍者，然后去健身房做同样的动作"
        ]
      },
      {
        title: "《非对称风险》",
        author: "纳西姆·尼古拉斯·塔勒布",
        times: "1",
        feel: ["时空的遍历性"]
      },
      {
        title: "《富人思维》",
        author: "贾森·卡拉卡尼斯",
        times: "1",
        feel: ["才可以"]
      },
      {
        title: "《四世同堂》",
        author: "老舍",
        times: "1",
        feel: ["那个时代的北京城"]
      },
      {
        title: "《明朝那些事儿》",
        author: "当年明月",
        times: "1",
        feel: ["投敌了", ""]
      },
      {
        title: "《月亮和六便士》",
        author: "威廉·萨默赛特·毛姆",
        times: "1",
        feel: ["艺术", "心智成熟度的人看", "枯燥后华丽而深远"],
        link: [
          "https://baike.baidu.com/tashuo/browse/content?id=6d6b44f741a7b31e15d81e4d&lemmaId=9521816&lemmaId=9521816&fr=qingtian"
        ]
      },
      {
        title: "《阅读是一座随身携带的避难所》",
        author: "威廉·萨默赛特·毛姆",
        times: "1",
        feel: ["观点永流传"]
      },
      {
        title: "《天龙八部》",
        author: "金庸",
        times: "1",
        feel: [
          "魔幻",
          "心魔，皇二代、武功超群，困于王姑娘",
          "萧峰死了，我哭了，侠之大者，为国为民。作者可以控制你"
        ]
      },
      {
        title: "《射雕英雄转》",
        author: "金庸",
        times: "1",
        feel: ["琴棋书画吃样样精通"]
      },
      {
        title: "《笑傲江湖》",
        author: "金庸",
        times: "1",
        feel: ["老炮"]
      },
      {
        title: "《鹿鼎记》",
        author: "金庸",
        times: "1",
        feel: ["不知出处的韦小宝，进步的历史观"]
      },
      {
        title: "《了不起的盖茨比》",
        author: "菲茨杰拉德",
        times: "1",
        feel: ["文字可以美妙到如此地步"]
      },
      {
        title: "《小王子》",
        author: "安托万·德·圣·埃克苏佩里",
        times: "1",
        feel: ["写个大人看的"]
      },
      {
        title: "《爱你就像爱生命》",
        author: "王小波",
        times: "1",
        feel: ["深情可穿千古，再长寿点就更好了"]
      },
      {
        title: "《一只特立独行的猪》",
        author: "王小波",
        times: "1",
        feel: ["老炮"]
      },
      {
        title: "《我的精神家园》",
        author: "王小波",
        times: "1",
        feel: ["老炮"]
      },
      {
        title: "《我决定活的有趣》",
        author: "蔡澜",
        times: "1",
        feel: ["老炮"]
      },
      {
        title: "《撒哈拉沙漠》",
        author: "三毛",
        times: "1",
        feel: ["老炮"]
      },
      {
        title: "《彼岸风景》",
        author: "俞敏洪",
        times: "1",
        feel: ["雨中的牛"]
      },
      {
        title: "《越简单，越美好》",
        author: "罗敷",
        times: "1",
        feel: ["有趣，长见识的书", "果子，派", "纹身奶爸", "恋人像室友"]
      },
      {
        title: "《这么慢，那么美》",
        author: "尤瓦尔·赫拉利",
        times: "1",
        feel: ["老炮"]
      },
      {
        title: "《至味在人间》",
        author: "陈晓卿",
        times: "1",
        feel: ["老炮"],
        feel: [
          "舌尖上的中国，烟火气。小众",
          "那个叔叔啥时候出现...",
          "我是那样的人"
        ]
      },
      {
        title: "《爱的多重奏》",
        author: "阿兰·巴迪欧",
        times: "1",
        feel: ["老炮"]
      },
      {
        title: "《穷查理宝典》",
        author: "查理·芒格",
        times: "1",
        feel: ["老炮"]
      },
      {
        title: "《如何让你爱的人爱上你》",
        author: "赫尔·郎兹",
        times: "1",
        feel: ["社交 关系"]
      },
      {
        title: "《男人来自火星，女人来自金星：修炼亲密关系的方法》",
        author: "约翰·格雷",
        times: "1",
        feel: ["亲密关系手册"]
      },
      {
        title: "《天才在左 疯子在右》",
        author: "高铭",
        times: "1",
        feel: ["彩色的蘑菇，我走进你心里你就能走进我", "他还在，你看他刚写的诗"]
      },

      {
        title: "《你有你的计划 世界另有计划》",
        author: "万维钢",
        times: "1",
        feel: ["猎鹰"]
      }
    ]
  }),
  methods: {
    goFeel(list){


      
    }
  },

  created() {
    this.tenBooks = this.books.slice(0, 10);
    this.otherBooks = this.books.slice(10);
  }
};
</script>