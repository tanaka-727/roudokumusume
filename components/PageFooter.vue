<template>
    <div class="scroll">
        <div class="footer">
            <section class="contact">
            <h2 class="title">Contact</h2>
              <p>お問い合わせ　　朗読むすめ事務局</p>
              <h3><a href="mailto:office@roudo9.com"><img src="/images/Mail.png" alt="メールアイコン" class="icon">office@roudo9.com</a></h3>
              <h3><a href="tel:03-6435-7748"><img src="/images/Tel.png" alt="電話アイコン" class="icon">03-6435-7748</a></h3>
              <p>担当：岡村</p>
            </section>
            <p class="copy">&copy;ジェーアールティー株式会社</p>
        </div>
    </div>
</template>

<style scoped>
/* 全体 */
*{
    margin: 0;
    padding: 0;
}
.scroll{
    display: block;
    width: 92.5vw;
    margin: 0 auto;
    height: 80px;
    max-width: 1000px;
}
.footer {
   height: 310px;   
}
/* コンタクト */
.contact {
background-color:   #fffbef;
height: 285px;
text-align: center;
}
.contact p {
    margin-top: 20px;
}
.icon {
    height: 32px;
    width: 32px;
    vertical-align: -10px;
    margin-top: 10px;
}
.contact a:hover {
    color:rgb(36, 196, 245);
}
/* コピーライト */
.copy {
    background-color: #f4e7d4;
    text-align: center;
    height: 25px;
    padding-top: 10px;
}
.title {
    color: #d45d5d;
    text-align: center;
    margin: 0;
    padding-top: 40px;
}
</style>