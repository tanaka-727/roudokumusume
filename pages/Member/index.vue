<!-- メンバー一覧ページ -->
<template>
 <div class="scroll">
    <main class="about">
       <h2 class="title">朗読むすめ　メンバー紹介</h2>
       <p>
        朗読むすめは、多彩なメンバーが集まった「声のプロ集団」。<br>
        また、「教育系朗読ユニット」の名にふさわしい才色兼備なメンバーが揃っています。<br><br>

        アナウンサー、声優、ラジオパーソナリティ、役者、日本語教師、ナレーター、アイドル <br>
        元スポーツキャスター、高校教師、MC、大学講師…など様々な場面で活躍。<br>
        個性あふれるメンバーを、是非ひとりひとりチェックしてみてくださいね。
         </p>
    </main>
      <div class="fullMember">
         <section class="announcerList">
            <h3 class="category"> アナウンサー </h3>
            <div class="announcerMember">
               <div v-for="member of announcer" :style="`background-color: ${member.memberColor}; border:10px solid ${member.memberColor}; border-radius:25% 10%;`" class="member__link">
               <nuxt-link :to="`/member/${member.id}`">
               <img :src="member.bustupPhoto.url" alt="" srcset="">
               <h3 class="text">{{ member.name }}</h3>
               <div v-html="member.job" class="text"></div>
               </nuxt-link>
               <audio controls :src="member.voiceSample"></audio>
               </div>
            </div>
         </section>

         <section class="joutyuunarratorList">
            <h3 class="category"> 常駐ナレーター </h3>

            <h4>- かわいい系Voice -</h4>
            <div class="cuteMember">
               <div v-for="member of cute" :style="`background-color: ${member.memberColor}; border:10px solid ${member.memberColor}; border-radius:25% 10%;`" class="member__link">
               <nuxt-link :to="`/member/${member.id}`">
               <img :src="member.bustupPhoto.url" alt="" srcset="">
               <h3 class="text">{{ member.name }}</h3>
               <div v-html="member.job" class="text"></div>
               <audio controls :src="member.voiceSample"></audio>
               </nuxt-link>
             </div>
            </div>

            <h4>- 元気系Voice -</h4>
            <div class="fineMember">
               <div v-for="member of fine" :style="`background-color: ${member.memberColor}; border:10px solid ${member.memberColor}; border-radius:25% 10%;`" class="member__link">
               <nuxt-link :to="`/member/${member.id}`">
                  <img :src="member.bustupPhoto.url" alt="" srcset="">
                  <h3 class="text">{{ member.name }}</h3>
                  <div v-html="member.job" class="text"></div>
                  <audio controls :src="member.voiceSample"></audio>
               </nuxt-link>
               </div>
            </div>

            <h4>- 落ち着き系Voice -</h4>
            <div class="coolMember">
               <div v-for="member of cool" :style="`background-color: ${member.memberColor}; border:10px solid ${member.memberColor}; border-radius:25% 10%;`" class="member__link">
               <nuxt-link :to="`/member/${member.id}`">
               <img :src="member.bustupPhoto.url" alt="" srcset="">
               <h3 class="text">{{ member.name }}</h3>
               <div v-html="member.job" class="text"></div>
               <audio controls :src="member.voiceSample"></audio>
               </nuxt-link>
               </div>
            </div>

            <h4>- 癒し系Voice -</h4>
            <div class="healingMember">
               <div v-for="member of healing" :style="`background-color: ${member.memberColor}; border:10px solid ${member.memberColor}; border-radius:25% 10%;`" class="member__link">
               <nuxt-link :to="`/member/${member.id}`">
               <img :src="member.bustupPhoto.url" alt="" srcset="">
               <h3 class="text">{{ member.name }}</h3>
               <div v-html="member.job" class="text"></div>
               <audio controls :src="member.voiceSample"></audio>
               </nuxt-link>
               </div>
            </div>

         </section>
     </div>

      <div class="supportmemberList">
      <h2 class="title">サポートメンバー</h2>
        <div class="supportmemberflex">
            <img src="/images/watatsumi.jpg" alt="綿津海うた" class="supportmember">
            <img src="/images/okamura.jpg" alt="岡村" class="supportmember">
            <img src="/images/nakayama.jpg" alt="中山" class="supportmember">
         </div>
      </div>
   </div>
</template>

<script setup lang="ts">
useHead({
   title: "メンバー紹介 | 朗読むすめ",
})

const runtimeConfig = useRuntimeConfig();

const { data } = await useFetch(`https://${runtimeConfig.public.serviceDomain}.microcms.io/api/v1/member?limit=100`,{
headers: {'X-MICROCMS-API-KEY':runtimeConfig.public.apiKey}}
)

console.log(data)
console.log(data.value.contents[0].category[0])
const announcer = data.value.contents.filter(content => content.category[0] == "アナウンサー");
const fine = data.value.contents.filter(content => content.category[0] == "元気系");
const cute = data.value.contents.filter(content => content.category[0] == "かわいい系");
const cool = data.value.contents.filter(content => content.category[0] == "落ち着き系");
const healing = data.value.contents.filter(content => content.category[0] == "癒し系");
</script>

<style scoped>
.about {
   padding-top: 80px;
   padding-bottom: 20;
   height: fit-content;
   background-color: #f4e7d4;
}
.fullMember section {
   background-color: #fffbef;
}
.fullMember h4 {
   color: #fff;
  font-size: 25px !important;
  text-shadow: 2px 1px 0 #000, -1px 1px 0 #000, 1px -1px 0 #000, -1px -1px 0 #000;
}
.fullMember h3 {
   font-family: "Zen Maru Gothic";
}
 .announcerMember, .fineMember, .cuteMember, .coolMember, .healingMember {
   display: flex;
   gap: 30px;
   padding: 0 30px;
   padding-bottom: 30px;
 }
 .member__link {
   width: calc(100% / 3);
 }
 .fineMember .member__link, .cuteMember .member__link {
   width: calc((100% - 120px) / 3);
 }
 /* 写真 */
.announcerList img {
   width: 100%;
   background-color: white;
   border-radius: 30% 10%;
}
.joutyuunarratorList img {
   width: 100%;
   background-color: white;
   border-radius: 30% 10%;
}
/* テキスト */
.category {
   padding: 30px 0;
   text-align: center;
   color: #d45d5d;
   font-size: 23px;
   font-family: "arial black";
}
h4 {
   padding-top: 20px;
   padding-bottom: 10px;
   padding-left: 60px;
   font-size: 20px;
}
.text {
   color: #000;
   text-align: center;
}
section a{
   text-decoration: none;
}
/* ボイス */
audio {
   padding-top: 5px;
   width: 93%;
}
/* サポートメンバー */
.supportmemberList {
   background-color: #f4e7d4;
   padding: 0 20px;
   padding-bottom: 30px;
}
.supportmemberflex {
   display: flex;
   flex-wrap: wrap;
   gap: 10px;
}
.supportmember {
   width: calc((100% - 10px) / 2);
   height: auto;
   margin-top: 20px;
   border-radius: 25px;
}
@media screen and (max-width:768px),print {
   .about {
      padding-top: 70px;
      padding-bottom: 0;
   }
   main p {
      padding: 20px;
    }
   .announcerMember, .fineMember, .cuteMember, .coolMember, .healingMember {
      flex-wrap: wrap;
   }
   .member__link {
      width: calc(80% / 2);
      margin: auto;
   }
   .fineMember .member__link, .cuteMember .member__link {
      width: calc(80% / 2);
      margin: auto;
   }
   .announcerList img {
   width:100%;
   background-color: white;
   border-radius: 30% 10%;
   }
   /* テキスト */
   .category {
   padding: 15px 0;
   }
   /* ボイス */
   audio {
   padding-top: 10px;
   width: 85%;
   padding-left: 10px;
   }

   /* サポートメンバー */
    .supportmemberflex {
      flex-direction: column;
    }
    .supportmember {
      width: 100%;
    }
}
@media screen and (max-width:545px),print {
   .announcerMember, .fineMember, .cuteMember, .coolMember, .healingMember {
      flex-direction: column;
   }
   .member__link {
      width: 80%;
      margin: auto;
   }
   .fineMember .member__link, .cuteMember .member__link {
   width: calc((100% - 90px));
   }
}
</style>