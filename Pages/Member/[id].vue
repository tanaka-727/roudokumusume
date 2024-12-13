<template>
    <div class="scroll">
        <main>
            <h2 class="title">プロフィール</h2>
            <div class="memberProfile">
                <img :src="`${data.bookPhoto.url}`" alt="">
                <dl class="profileText">
                    <dt>Name</dt>
                    <dd>{{ data.nameEnglish }}</dd>
                    <dd class="name">{{ data.name }}</dd> 
                    <dt>Job</dt>
                    <dd v-html="data.job"></dd>
                    <dt>Voice</dt>
                    <dd v-html="data.Voice"></dd>
                    <dt>SNS</dt>
                    <dd v-html="data.sns"></dd>
                    <dt>YouTube</dt>
                    <dd v-html="data.YoutubeLink"></dd>
                </dl>
            </div>
            <div class="youtube__box">
                <div v-html="data.youtubeThumbnail" class="thumbnail"></div>
            </div>
        </main>

        <section class="roudokujob">
            <h2 class="title">朗読むすめでの活動・お仕事</h2>
            <h4>書籍</h4>
            <div class="bookList">
              <div v-for="book of data.workBook">
                 <img :src="`${book.url}`" alt="" class="bookimg">
              </div>
            </div>
            <div v-html="data.roudokuWorks" class="roudokuWorks"></div>
        </section>
    
        <section class="career">
            <h2 class="title">経歴</h2>
            <div v-html="data.career" class="careerText"></div>
        </section>
    </div>
</template>


<!-- スクリプト -->
<script setup>
const route = useRoute();
const id = route.params.id;

const runtimeConfig = useRuntimeConfig();

const { data } = await useFetch(`https://${runtimeConfig.public.serviceDomain}.microcms.io/api/v1/member/${id}`,{
headers: {'X-MICROCMS-API-KEY':runtimeConfig.public.apiKey}}
)
</script>


<!-- ｃｓｓ -->
<style scoped>
* {
    margin: 0;
    padding: 0;
    /* font-family:'M PLUS Rounded 1c', sans-serif; */
    /* font-family: 'Noto Sans JP", sans-serif'; */
}
.scroll{
    display: block;
    margin: 0 auto;
    width: 92.5vw;
    height: 100%;
    max-width: 1000px;
}
/* プロフィール */
main {
    padding-top: 80px;
    background-color: #f4e7d4;
    height: fit-content;
}
.title {
    color: #d45d5d;
    text-align: center;
    margin: 0;
    padding-top: 40px;
    margin-bottom: 10px;
}
.memberProfile {
    display: flex;
    margin-top: 3%;
    padding: 0 80px;
}
.memberProfile img {
    width: 340px;
    height: 450px;
    border-radius: 20px;
    background-color: #fff;
    object-fit: cover;
}
.profileText  {
   width: 520px;
   margin-top: 50px;
   text-align: center;
}
.profileText .name {
    font-size: 40px;
    font-weight: bold;
}
.profileText dt {
    float: left;
    clear: left ;
    margin-left: 70px;
    margin-right: 0.5em ;
    margin-top: 30px;
}
.profileText dd {
    margin-left: 100px ;
    margin-top: 5px;
}
.youtube__box {
    max-width: 700px;
    margin: auto;
    aspect-ratio: 16 / 9;
}
.thumbnail{
    /* width: 700px; */
    /* height: 390px; */
    width: 100%;
    height: 100%;
    margin: 0 auto;
    padding-top: 30px;
    padding-bottom: 30px;
}
/* 朗読むすめでの活動・お仕事 */
.roudokujob {
    background-color: #fffbef;
    height: fit-content;
    padding-bottom: 3%;
}
.roudokujob h4 {
    margin-left: 80px;
}
.bookList {
    display: flex;
    margin: 40px;
}
.bookimg  {
width: 140px;
height: 200px;
margin-left: 40px;
}
.roudokuWorks {
    margin-left: 80px;
}

/* 経歴 */
.career {
    height: fit-content;
    padding-bottom: 3%;
}
.careerText {
    margin-left: 80px;
}
@media screen and (max-width:768px) {
    .memberProfile {
        flex-direction: column;
    }
}
</style>