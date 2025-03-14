<!-- お仕事紹介ページ -->
<template>
        <div class="scroll">
           <main>
            <h2 class="title">これまでのお仕事</h2>
            <p>
                朗読むすめは、これまで数々のクライアントワークを行ってきました。<br><br>
                書籍付属音声はもちろん、出版社様や企業様とコラボしたPR音声、書店様に設置するPOPやQRコード、<br>
                さらにはキャラクターボイスやオーディオブックなど内容は多岐にわたります。<br><br>
                そして、朗読部屋Sutudioを設立してからは、収録から納品まで全てを自社で行ってきました。<br><br>
                ナレーター、エンジニア、編集担当、事務スタッフ、運営、全てを自社で完結させれられる朗読むすめ<br>
                にお任せ頂ければ、確かなクオリティを素早くお届けいたします。
            </p>
           </main> 
           <ul class="works">
             <li>
                 <img src="/images/nendaianpu.jpg" alt="東進ブックス様/「なぜ」と「流れ」でおぼえる日本史年代暗譜" class="images">
                 <div class="worktext">
                     <h3>東進ブックス様 / 書籍付属音声</h3>
                     <p>「「なぜ」と「流れ」でおぼえる日本史年代暗譜」</p>
                 </div>
              </li>
              <li>
                 <img src="/images/nihonshi200.png" alt="ベレ出版様/「日本史の200人」一問一答" class="images">
                 <div class="worktext">
                     <h3>ベレ出版様 / 書店PR音声</h3>
                     <p>「教養として知っておきたい「日本史の200人」一問一答」</p>
                 </div>
             </li>
              <li>
                 <img src="/images/mensetu.jpg" alt="Gakken様/高校入試面接対策をひとつひとつわかりやすく。" class="images">
                 <div class="worktext">
                     <h3>Gakken様 / 書籍付属音声</h3>
                     <p>「高校入試　面接対策をひとつひとつわかりやすく。」</p>
                 </div>
             </li>
             <li>
                 <img src="/images/rekisinonaze.jpg" alt="増新堂・受験研究社様/歴史のなぜ？新辞典" class="images">
                 <div class="worktext">
                     <h3>増新堂・受験研究社様 / 書店QR・POP作成</h3>
                     <p>「小学自由自在　歴史のなぜ？新辞典」</p>
                 </div>
             </li>
             <li>
                 <img src="/images/kyotutest.jpg" alt="文英堂様/共通テストはこれだけ！日本史B" class="images">
                 <div class="worktext">
                     <h3>文英堂様 / 書店フォトフレーム作成</h3>
                     <p>「共通テストはこれだけ！日本史B」</p>
                 </div>
             </li>
              <li>
                 <img src="/images/audio_bunkashi.jpg" alt="東進ブックス様/金谷の日本史「なぜ」と「流れ」が分かる本" class="audioBook">
                 <div class="worktext">
                     <h3>東進ブックス様 / オーディオブック音声</h3>
                     <p>「金谷の日本史「なぜ」と「流れ」が分かる本」</p>
                 </div>
             </li>    
             <li>
                 <img src="/images/sokudoku.png" alt="ワニブックス様/速読日本史" class="images">
                 <div class="worktext">
                     <h3>ワニブックス様 / 書籍付属音声</h3>
                     <p>「2倍速で読めて、忘れない　速読日本史」</p>
                 </div>
             </li>
             <li>
                 <img src="/images/nihonshinojugyou.jpg" alt="祥伝社様/「日本史の授業」" class="images">
                 <div class="worktext">
                     <h3>祥伝社様 / 書店フォトフレーム作成</h3>
                     <p>「日本人なら知っておきたい日本史の授業」</p>
                 </div>
             </li>
             <li>
                 <img src="/images/online.png" alt="東進ブックス様/みんなの一問一答オンライン" class="online">
                 <div class="worktext">
                     <h3>東進ブックス様 / キャラクターボイス声優</h3>
                     <p>「みんなの一問一答オンライン」</p>
                 </div>
             </li>
             <li>
                 <img src="/images/irimonnittou3rd.jpg" alt="東進ブックス様/日本史一問一答【完全版】3rd edition" class="images">
                 <div class="worktext">
                     <h3>東進ブックス様 / 書籍付属音声</h3>
                     <p>「日本史一問一答【完全版】3rd edition」</p>
                 </div>
             </li>
             <li>
                 <img src="/images/kyoututest2024.jpg" alt="文英堂様/共通テストはこれだけ！日本史" class="images">
                 <div class="worktext">
                     <h3>文英堂様 / 書籍付属音声</h3>
                     <p>「共通テストはこれだけ！日本史」</p>
                 </div>
             </li>
             <li>
                 <img src="/images/sekaishi.jpg" alt="東進ブックス様/「世界史一問一答【完全版】4th edition" class="images">
                 <div class="worktext">
                     <h3>東進ブックス様 / 書籍付属音声</h3>
                     <p>「世界史一問一答【完全版】4th edition」（監修 加藤和樹）</p>
                 </div>
             </li>
           </ul>
        </div>
</template>

<style scoped>
/* メイン（about） */
main {
    background-color: #f4e7d4;
    display: block;
    height: fit-content;
    padding-top: 80px;
}
/* ワーク */
.works {
    background-color: #fffbef;
    height: fit-content;
    padding: 20px;
}
.works img {
    height: 200px;
    width: 140px;
}
.works .audioBook {
    height: 180px;
    width: 180px;
}
.works .online {
    height: 170px;
    width: 150px;
}
.worktext {
    margin-left: 30px;
    margin-top: 10%;
}
.works li {
    display: flex;
    margin: 5%;
    margin-left: 20%;
}
@media screen and (max-width:768px),print {
    main {
        padding-top: 70px;
        padding-bottom: 15px;
    }
    main p {
        padding: 20px;
    }
    .works img {
        margin: 0 auto;
    }
    .works li {
        flex-direction: column;
        text-align: center;
        margin-left: 0;
        margin-bottom: 50px;
    }
    .works li:last-child {
        margin-bottom: 0;
    }
    .worktext {
        margin-left: 0;
        margin-top: 10px;
    }
}
</style>

<script setup>
useHead({
    title: "これまでのお仕事 | 朗読むすめ",
})
</script>