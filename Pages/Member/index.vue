<!-- メンバー一覧ページ -->
<template>
 <div class="scroll">
    <main class="about">
       <h2 class="title">朗読むすめ　メンバー紹介</h2>
       <p>
        朗読むすめは、多彩なメンバーが集まった「声のプロ集団」。<br>
        また、「教育系朗読ユニット」の名にふさわしい才色兼備なメンバーが揃っています。<br>
        アナウンサー、声優、ラジオパーソナリティ、役者、日本語教師、ナレーター、アイドル <br>
        元スポーツキャスター、高校教師、MC、大学講師など様々な場面で活躍。<br>
        個性あふれるメンバーを、是非ひとりひとりチェックしてみてくださいね。
      </p>
    </main>
    <section class="fullMember">
         <div v-for="member of data.contents" :style="`background-color: ${member.memberColor}; border:10px solid ${member.memberColor}; border-radius:25% 10%;`" class="member__link">
            <nuxt-link :to="`/member/${member.id}`">
               <img :src="member.bustupPhoto.url" alt="" srcset="">
               <h3 class="text">{{ member.name }}</h3>
               <div v-html="member.job" class="text"></div>
          </nuxt-link>
         </div>
         <!-- {{ data.contents}} -->
      </section>
 </div>
</template>

<script setup lang="ts">
const runtimeConfig = useRuntimeConfig();

const { data } = await useFetch(`https://${runtimeConfig.public.serviceDomain}.microcms.io/api/v1/member?limit=100&orders=createdAt`,{
headers: {'X-MICROCMS-API-KEY':runtimeConfig.public.apiKey}}
)

// console.log(data)
</script>

<style scoped>
.about {
   padding-top: 80px;
   height: fit-content;
   background-color: #f4e7d4;
}
.fullMember {
   padding:  0 63px;
   height: fit-content;
   display: grid;
   grid-template-columns: repeat(3,1fr);
   gap: 30px;
   padding-bottom: 20px;
}
.fullMember img{
   width: 250px;
   background-color: white;
   border-radius: 25% 10%;
}
.text {
   color: #000;
   text-align: center;
}
section a{
   text-decoration: none;
}
@media screen and (max-width:768px),print {
   main p {
      padding: 20px;
    }
    .fullMember {
   padding:  0 10px;
   height: fit-content;
   display: grid;
   grid-template-columns: repeat(1,1fr);
   gap: 20px;
   padding-bottom: 10px;
   }
   .fullMember img{
   width: 250px;
   background-color: white;
   border-radius: 25% 10%;
}
   .member__link{
      margin: auto;
   }
}
@media screen and (max-width:1020px){
   .fullMember {
   padding:  0 10px;
   height: fit-content;
   display: grid;
   grid-template-columns: repeat(2,1fr);
   gap: 20px;
   padding-bottom: 20px;
   }
   .member__link{
      margin: auto;
   }
}
</style>