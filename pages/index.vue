<!-- トップページ -->
<template>
        <div class="scroll">
            <h1><img src="/images/topimage.jpg" alt="朗読むすめメンバー集合写真 田辺桃菜、辻紗樹、三浦菜摘、美波花音、山城綺奈、湯本佳月、曽根さとみ、石井るい。堀宮菜々子、守谷藍、青木めぐ、松尾有紀、萬海歌" class="topimage"/></h1>
            <!-- メイン（about） -->
            <main>
                <h2 class="title">About</h2>
                <p class="index_mainp">「朗読むすめ」は、教育・歴史・古典を中心とした朗読ユニットです。<br>
                    300名近いオーディションから選ばれました。<br>2021年11月3日に結成。<br><br>
                    オーディオブック、書籍の付属音声、物語の読み聞かせなど
                    <br>「声」で勝負する朗読ユニットです。<br>
                    <br>監修は、歴史コメンテーターの金谷俊一郎先生。<br>
                    これまで携わってきたお仕事は多岐にわたります。
                </p>  
                <img src="/images/minikanaya.png" alt="金谷俊一郎先生" class="minikanaya">
                <div class="cardList">
                  <ul>
                    <li><img src="/images/nihonshi200.png" alt="日本史の200人一問一答"></li>
                    <li><img src="/images/sokudoku.png" alt="速読日本史"></li>
                    <li><img src="/images/ichimonittou_3.png" alt="日本史一問一答"></li>
                    <li><img src="/images/mensetu.jpg" alt="面接対策をひとつひとつわかりやすく。"></li>
                    <li><img src="/images/nendaianpu.jpg" alt="なぜと流れがわかる本"></li>
                    <li><img src="/images/sekaishi.jpg" alt="世界史一問一答"></li>
                    <li><img src="/images/kyotutest.jpg" alt="共通テストBlue"></li>
                    <li><img src="/images/rekisinonaze.jpg" alt="歴史のなぜ？新辞典"></li>
                    <li><img src="/images/nazetonagare2024.jpg" alt="なぜと流れ2024"></li>
                    <li><img src="/images/nihonshinojugyou.jpg" alt="日本史の授業"></li>
                    <li><img src="/images/irimonnittou3rd.jpg" alt="一問一答3red"></li>
                    <li><img src="/images/kyoututest2024.jpg" alt="共通テスト2024"></li>
                    <li><img src="/images/nihonshi200.png" alt="日本史の200人一問一答"></li>
                    <li><img src="/images/sokudoku.png" alt="速読日本史"></li>
                    <li><img src="/images/ichimonittou_3.png" alt="日本史一問一答"></li>
                    <li><img src="/images/mensetu.jpg" alt="面接対策をひとつひとつわかりやすく。"></li>
                    <li><img src="/images/nendaianpu.jpg" alt="なぜと流れがわかる本"></li>
                    <li><img src="/images/sekaishi.jpg" alt="世界史一問一答"></li>
                    <li><img src="/images/kyotutest.jpg" alt="共通テストBlue"></li>
                    <li><img src="/images/rekisinonaze.jpg" alt="歴史のなぜ？新辞典"></li>
                    <li><img src="/images/nazetonagare2024.jpg" alt="なぜと流れ2024"></li>
                    <li><img src="/images/nihonshinojugyou.jpg" alt="日本史の授業"></li>
                    <li><img src="/images/irimonnittou3rd.jpg" alt="一問一答3red"></li>
                    <li><img src="/images/kyoututest2024.jpg" alt="共通テスト2024"></li>
                  </ul>
                </div>
                <p class="index_mainp">担当するのは書籍付属音声にとどまらず、PR動画＆音声、書店に設置するPOPやQRコードの作成、<br> さらにはキャラクターボイスやオーディオブックなど様々です。</p>
            </main>
            <!-- セクション（SNS） -->
            <section>
                <h2 class="title">SNS</h2>
                <div class="YouTube">
                  <h3><a href="//www.youtube.com/channel/UC7-LptSjwFKrtwuBrzsXKgA"><img src="/images/YouTube.png" alt="YouTubeアイコン" class="icon">YouTube</a></h3>
                  <p>【かなや放送と朗読むすめ】登録者数１万人突破！</p>
                </div>
                <div class="youtube__box">
                 <iframe width="560" height="315" src="https://www.youtube.com/embed/vktWEUfOVW4?si=X9liu--MAw7L4gYn" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                </div>
                <div class="iconList">
                  <h3><a href="https://x.com/roudokumusume/"><img src="/images/X.png" alt="Xアイコン" class="icon">X</a></h3> 
                  <h3><a href="//www.instagram.com/rodokumusume/"><img src="/images/Instagram.png" alt="Instagramアイコン" class="icon">Instagram</a></h3>
                  <h3><a href="https://www.tiktok.com/@kanayadesu"><img src="/images/TikTok.png" alt="TikTokアイコン" class="icon">TikTok</a></h3>
                </div>
            </section>
        </div>
</template>


<style>
/* -----------
全体 
--------------*/
* {
    margin: 0;
    padding: 0;
    font-family:'M PLUS Rounded 1c', sans-serif;
}
body {
    background-color: #ffdea9;
    max-width: 1080px;
    margin: 0 auto;
}
.scroll{
    display: block;
    margin: 0 auto;
    width: 92.5vw; 
    height: 100%;  
    max-width: 1000px;
}
.title {
    color: #d45d5d;
    text-align: center;
    margin: 0;
    padding-top: 40px;
    font-size: 30px;
    font-family: "arial black" ,Helvetica, sans-serif;
}
/* トップイメージ */
.topimage {
    padding-top: 80px;
    display: block;
    max-width: 100%;
	width: 100%;
    width: 1000px;
    height: auto;
}
/* メイン（about） */
main {
    background-color: #fffbef;
    display: block;
    height: fit-content;
    padding-bottom: 30px;
    position: relative;  
    width: 100%;
    overflow: hidden;
}
main p {
    text-align: center;
    padding-top: 20px;
}
.minikanaya{
    width: 370px;
    height: 260px;
    position:absolute;
    top: 76px;
    left: 660px;
    display: block;
}
/* 画像ループ */
.cardList {
	/* overflow: hidden; */
    padding-top: 20px;
}
.cardList ul {
	animation: marquee-right 30s linear infinite;
	display: flex;
	margin: 0;
	padding: 0;
	width: max-content;
}
.cardList ul li {
	list-style: none;
	padding: 10px 15px;
}
.cardList img {
	display: block;
    height: 200px;
	width: 140px;
}
@keyframes marquee-right {
	from {
		transform: translateX(0%);
	}
	to {
		transform: translateX(-50%);
	}
}
/* -------------
セクション（SNS） 
-----------------*/
section {
    background-color: #f4e7d4;
    height: fit-content;
}
.YouTube {
    display: flex;
    padding-left: 5%;
    margin-top: 7px;
    margin-bottom: 10px;
}
.youtube__box {
    max-width: 560px;
    margin: auto;
    aspect-ratio: 16 / 9;
}
.youtube__box iframe {
    width: 100%;
    height: 100%;
}
.YouTube p {
    padding-top: 11px;
    margin-left: 30px;
}
.icon {
    width: 45px;
    height: 45px;
    vertical-align: -15px;
}
.iconList {
    display: flex;
    justify-content: space-between;
    padding-left: 15%;
    padding-right: 15%;
    padding-bottom: 10px;
    margin-top: 20px;
}
.iconList a:hover {
    color: #d45d5d;
}
iframe {
    display: block;
    margin: 0 auto;
}
h3 a {
    text-decoration: none;
    color: #000;
    margin-right: 5px;
}
@media screen and (max-width:768px) {
    .topimage {
        padding-top: 70px;
    }
    .index_mainp {
        padding-right: 20px;
        padding-left: 20px;
    }
    .YouTube{
        flex-direction: column;
    }
    .title {
    padding-top: 20px;
    font-size: 24px;
    }
    main p {
    text-align: left;
    }
    .YouTube p {
        margin-left: 0;
    }
}
@media screen and (max-width:992px) {
    .minikanaya {
        display: none
    }
}
</style>