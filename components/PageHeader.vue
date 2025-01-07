<template>
    <div class="scroll">
        <div class="header">
            <nav>
              <ul>
                <li><nuxt-link :to="`/`">
                    <img src="/images/logo.png" alt="朗読むすめロゴ" class="logo">
                </nuxt-link></li>
                 <li><nuxt-link :to="`/studio/`"><img src="/images/Mike.png" alt="マイクのアイコン" class="icon">Studio</nuxt-link></li>
                 <li><nuxt-link :to="`/Member/`"><img src="/images/Member.png" alt="メンバーのアイコン" class="icon">Member</nuxt-link></li>
                 <li><nuxt-link :to="`/youtube`"><img src="/images/YouTube.png" alt="Youtubeのアイコン" class="icon">YouTube</nuxt-link></li>
                 <li><nuxt-link :to="`/news`"><img src="/images/News.png" alt="ニュースのアイコン" class="icon">News</nuxt-link></li>
                 <li><nuxt-link :to="`/Works`"><img src="/images/Works.png" alt="Worksのアイコン" class="icon">Works</nuxt-link></li>
             </ul>
           </nav>
        </div>
    </div>
</template>

<script setup>
</script>

<style scoped>
/* 全体 */
*{
    margin: 0;
    padding: 0;
}
.header {
    display: block;
    max-width: 1000px;
    width: 92.5vw;
    height: fit-content;
    position: fixed;
    z-index: 1;
}
/* ロゴ */
.logo {
    width: 80px;
    height: 80px;
}
/* ナビ */
nav ul {
    display: flex;
    margin: 0;
    padding: 0;
    width: 100%;
    height: 80px;
    overflow: hidden;
}
nav ul li {
    list-style: none;
    width: calc((92.5vw - 80px) /5);
    background-color: #fffbef;
    text-align: center;
    padding-top: 17px;
}
nav ul li:hover {
  background: #ffdea9;
  letter-spacing: 0.15em;
  transition: .2s
}
nav ul li a {
    text-decoration: none;
    color: #000;
    padding: 0;
    margin: 0;
    height: fit-content;
}
nav ul li:has(a .logo){
    width: fit-content;
    height: fit-content;
    padding: 0;
}
@media screen and (max-width:768px),print {
    .logo {
    width: 70px;
    height: 70px;
    }
    nav ul {
    height: 70px;
}
    nav ul li {
        width: calc((92.5vw - 70px) /5);
        padding-top: 2px;
        font-size: 12px;
    }
    .icon {
    display: block;
    margin: auto;
}
}
</style>