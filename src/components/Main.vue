<template lang="pug">
<div class='content-wrapper'>
    <div id="Contest">
        <a href="#MenuBlock"> <div id="BackToMenuButton"> </div> </a>
        <div id="Main">
            <div id="leftMain">

                <div id="leftText">
                    p.textMargin#TitlePlatform платформа
                    p.textMargin#TitleMathPlace MathPlace
                    <h3 class="textMargin" style="color:#525252; font-family: 'Roboto', sans-serif; font-size: 1.4em;" id="leftTextDiscrib">место, где вы можете с легкостью поднять свой уровень по математике</h3>
                    router-link.button.designButtonLesson.goButton(to='/main') Начать!
                </div>
                <img id="imgMain" src="./images/mainPhones.png" alt="Второй текст"/>
            </div>
        </div>
        <div id="Feature">
            <div class="Main2">
                p.boldText Что такое MathPlace? 🤔
                <p id="FeatureText"> Многофункциональная и гибкая платформа для изучения и размещения образовательных уроков по математике.  <strong style='color: black'>Просто, быстро, удобно</strong></p>
                //- <div id="design5" class="gradient"></div>
                div.AllAdvantages
                    div.Advantage
                        .Advantages
                            md-icon.md-size-3x.my-icon people
                            strong Большая аудитория
                            p Больше 2000 пользователей используют MathPlace для обучения
                    div.Advantage
                        .Advantages
                            md-icon.md-size-3x.iconAdvantege smartphone
                            strong Мобильное приложение
                            p Ученики могут обучаться в удобном приложение MathPlace для Android или на
                    div.Advantage
                        .Advantages
                            md-icon.md-size-3x.iconAdvantege edit
                            strong Удобный конструктор
                            p Разработали удобный конструктор для организации дистанционного образования

            </div>
        </div>
        p.MainScreen
            img(src="./images/main_screen.png")
        <div id="Feature">
            p.halfboldText Занимайтесь математикой <br>в удобных условиях 😎
            div.AllVerticalLines
                div.verticalBlock
                    img.LeftBigImage(src="./images/second_step.png")
                    div.RightVerticalText
                        strong.halfboldTextVertical Смотрите <br>нужные уроки
                        p.halfRegularTextVertical Полезные уроки от школьной математики до экзаменов и олимпиад. <br>Найдется то, что вам нужно
                div.verticalBlock
                    img.RightBigImage(src="./images/first_step.png")
                    div.LeftVerticalText
                        strong.halfboldTextVertical Изучайте математику <br>в привычном формате
                        p.halfRegularTextVertical Смотрите теорию, а затем решайте несколько задач для закрепления пройденного материала
                div.verticalBlock
                    img.LeftBigImage(src="./images/first_step.png")
                    div.RightVerticalText
                        strong.halfboldTextVertical Отслеживайте статистику <br>и двигайтесь дальше
                        p.halfRegularTextVertical Смотрите статистику по пройденным урокам, выполняйте достижения и следите за рейтингом
        </div>
        p.MainScreen
            img(src="./images/main_screen3.png")
        div.AllAdvantages
            p.halfboldText MathPlace охватывает 🔥
            div.MenuBlockMain
                .MenuBlockTopic
                    p.AlignCenter
                        img.MenuButton(src="./images/examination.png")
                    p Подготовку к экзаменам
            div.MenuBlockMain
                .MenuBlockTopic
                    p.AlignCenter
                        img.MenuButton(src="./images/school.png")
                    p Школьную программу
            div.MenuBlockMain
                .MenuBlockTopic
                    p.AlignCenter
                        img.MenuButton(src="./images/brain.png")
                    p <br>Олимпиады<br>
        </div>
        p.MainScreen
            img(src="./images/mainLabtop.png")

        <div id="Feature">
            <div class="Main2">
                <p id="FeatureText"><strong>Станьте автором</strong> открытого урока или проводите обучение в закрытых группах. MathPlace — удобный сервис для дистанционного преподавания</p>
            </div>
            div.AllAdvantages
                div.Advantage
                    .Advantages
                        md-icon.md-size-3x.my-icon class
                        strong Классы
                        p Доступ к результатм и полной статистике своих учеников в своих курсах

                div.Advantage
                    .Advantages
                        md-icon.md-size-3x.my-icon chat
                        strong Общение
                        p Общайтесь при помощи чата и создавайте группы класса
                div.Advantage
                    .Advantages
                        md-icon.md-size-3x.my-icon verified_users
                        strong Приватные курсы
                        p Закрытые курсы, доступ к которым предоставляет только их автор
        </div>
        .AlignCenterButton
            router-link.button.designButtonLesson.goButton(to='/teacher') Стать автором

        <div id="Task">
            //- <div id="design4" class="gradient"></div>
            p.halfboldText Проверьте свои силы 👇🏻
            div.MainTask.verticalBlock
                <div id="TaskText">
                    <p id="TextTask2">Для экзамена подготовили билеты с номерами от 1 до 50. Какова вероятность того, что наугад взятый учеником билет имеет однозначный номер?</p>
                </div>
                <div id="rightTask">
                    <input type="text" id="TaskIn" v-model="answer" :class = "{ answerCorrect : this.state === 1, answerWrong : this.state === 2 }">
                    <a href="#Task-Button">
                        div#TaskButton(@click="sendAnswer")
                            p#TaskButtonText Отправить
                    </a>
                </div>
        </div>
        <div id="DownloadPlayMarket" >
            //- img.imgFull(src="https://static.tildacdn.com/tild3436-6361-4632-b263-323966316338/A10.svg")
            p.textPlayMarket Попробуйте наше обновленное мобильное приложение
            img.imgPlayMarket(src="https://static.tildacdn.com/tild3533-6437-4834-b338-643133363864/googleplaybadge_en.png")
        </div>
        <div id="AboutDevelopers">
            <img id="finishImg" src="./images/final_screen.png" />
            <div id="finish">
                <h1 id="finishTitle">Посмотрите на <br>платформу в деле</h1>
                <p id="finishText">У нас есть уроки для всех от начинающих до профи.</p>
                .AlignCenterButton2
                    router-link.button.designButtonLesson.goButton(to='/main') Начать!
            </div>
        </div>
        <div id="AboutUs">
            p.halfboldText Следите за нашими новостями 👇🏻
            <div id="Media">
                <a href="https://vk.com/mathplace">
                    img#social(src="./images/vk_site.png")
                </a>
                <a href="https://www.instagram.com/ledokol_team/">
                    img#social(src="./images/inst_site.png")
                </a>
            </div>
        </div>
    </div>
</div>

</template>

<script>
export default {
  data () {
    return {
      state: 0,
      answer: ''
    }
  },
  methods: {
    sendAnswer () {
      if (this.answer === '0.18' || this.answer === '0,18') this.state = 1
      else this.state = 2
    }
  }
}

</script>

<style lang="stylus" scoped>

#TitlePlatform
    position relative
    color: #525252;
    font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
    font-size: 1.5em;
    font-weight: bold;

#TitleMathPlace
    position relative
    color #763DCA;
    font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
    font-size: 4em;
    font-weight: bold;
p
  letter-spacing auto !important

.designButtonLesson
  text-decoration none !important
  padding-top 12.5px
  position relative
  height 50px
  width 300px
  border: 2px solid #763DCA;
  border-radius 50px
  font-weight 550
  margin-left 20px
  color #763DCA !important
  background-color #FFFFFF
  opacity 0.8
  transition: 0.6s;
  text-align center
  vertical-align middle
.designButtonLesson:hover
  transition: 0.6s;
  color #FFFFFF !important
  background-color #763DCA

.AllVerticalLines

    width 70%
    margin-top 100px
    margin-left 15%
    @media screen and (max-width: 1200px) {
        margin-left 5%
        width 90%
    }

.verticalBlock
    height auto
    display: block;
    margin-top 150px
.verticalBlock:after
    content: "";
    display: block;
    clear: both;
    visibility: hidden;
    line-height: 0;
    height: 0;
    margin: 0;
    padding: 0;
.AlignCenter
    text-align center
.AlignCenterButton
    position relative
    margin-top 30px
    text-align center
.AlignCenterButton2
    position relative
    margin-top 30px
    margin-left 0px
    @media screen and (max-width: 1030px) {
        position relative
        margin-top 30px
        text-align center
    }
.MainScreen
    text-align center
    img
        margin-top 200px
        margin-bottom 100px
        width 80%
.LeftBigImage
    height auto
    width 50%
    display inline-block
    @media screen and (max-width: 1400px) {
        margin-top 60px
        width 40%
    }
    @media screen and (max-width: 850px) {
        margin-top 60px
        width 80%
        margin-left 10%
    }
.RightBigImage
    height auto
    width 50%
    align right
    float right
    text-align right
    @media screen and (max-width: 1400px) {
        width 40%
    }
    @media screen and (max-width: 850px) {
        margin-top 60px
        width 80%
        margin-left 10%
        float left
    }

.RightVerticalText
    height auto
    float right
    display inline-block
    margin-top 50px
    max-width 450px
    margin-bottom 0px
    @media screen and (max-width: 850px) {
        max-width 4500px
        margin-left 10%
    }
.LeftVerticalText
    height auto
    display inline-block
    margin-top 50px
    max-width 400px
    margin-bottom 0px
    @media screen and (max-width: 850px) {
        max-width 4500px
        width 80%
        margin-left 10%
    }
.halfboldTextVertical
    position relative
    width auto
    height auto
    color #525252
    text-align left
    font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
    font-size 27pt
    font-weight 400
.halfRegularTextVertical
    position relative
    width auto
    height auto
    text-align left
    font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
    font-size 15pt
    margin-top 20px
    font-weight 300
.goButton
    position relative
    height auto
    widht 1000px
    border: 2px solid #763DCA !important
    border-radius 50px
    font-weight 550
    color #763DCA
    background-color #EEE0FB
    opacity 0.9
    transition: 0.6s;
    text-align center
    vertical-align middle
.goButton2
    position relative
    height auto
    border: 2px solid #763DCA;
    border-radius 50px
    font-weight 550
    color #763DCA
    background-color #EEE0FB
    opacity 0.9
    font-size 14pt
    transition: 0.6s;
    text-align center
.alignCenter
    position relative
    width auto
    left 30%
    vertical-align middle
    text-align center
    margin 50px 0px
.goButton:hover
    transition: 0.6s;
    color #FFFFFF
    background-color #763DCA !important
.goButton
    margin-left 20px
    font-size 24pt

div
    line-height normal !important
    font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif

.answerCorrect
  background rgba(0, 255, 0, .5)
.answerWrong
  background rgba(255, 0, 0, .5)

#Content
    position absolute
    width 100%
    height auto

.content-wrapper
    // clear both
    position absolute
    display block
    width 100%
    background-image: radial-gradient(circle at 69% 86%, rgba(165, 165, 165,0.06) 0%, rgba(165, 165, 165,0.06) 25%,rgba(193, 193, 193,0.06) 25%, rgba(193, 193, 193,0.06) 50%,rgba(221, 221, 221,0.06) 50%, rgba(221, 221, 221,0.06) 75%,rgba(249, 249, 249,0.06) 75%, rgba(249, 249, 249,0.06) 100%),radial-gradient(circle at 49% 76%, rgba(129, 129, 129,0.06) 0%, rgba(129, 129, 129,0.06) 25%,rgba(164, 164, 164,0.06) 25%, rgba(164, 164, 164,0.06) 50%,rgba(200, 200, 200,0.06) 50%, rgba(200, 200, 200,0.06) 75%,rgba(235, 235, 235,0.06) 75%, rgba(235, 235, 235,0.06) 100%),radial-gradient(circle at 22% 64%, rgba(173, 173, 173,0.06) 0%, rgba(173, 173, 173,0.06) 25%,rgba(119, 119, 119,0.06) 25%, rgba(119, 119, 119,0.06) 50%,rgba(64, 64, 64,0.06) 50%, rgba(64, 64, 64,0.06) 75%,rgba(10, 10, 10,0.06) 75%, rgba(10, 10, 10,0.06) 100%),linear-gradient(307deg, rgb(255,255,255),rgb(255,255,255));
.MenuBlockMain
    position relative
    display inline-block
    width 30%
    min-width 250px
    height auto
    margin-left 10px
    margin-right 10px
.MenuBlockTopic
    position relative
    display inline-block
    width 80%
    min-width 250px
    height auto
    margin-top 80px
    margin-left 10%
    margin-right 10%
    box-shadow 0px 0px 5px 0px #aaaaaa
    border-radius 20px
    transition 0.2s

    @media screen and (max-width: 450px) {
        display inline-block
        width 100%
        min-width 100px
    }

    p
        width auto
        text-align center
        font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
        font-size 27pt
        font-weight 400
        margin-top 50px
        color #000000
        margin-left 10px
        margin-right 10px
        margin-bottom 30px

.MenuBlockTopic:hover
    box-shadow 0px 0px 12px 3px #bbbbbb

.halfboldText
    width 100%
    height auto
    margin-top 10%
    margin-bottom 0px
    text-align center
    color #525252
    font-color #525252
    text-color #525252
    font-family "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
    font-size 44px
    font-weight 400
.boldText
    width 100%
    height auto
    margin-top 10%
    // color #525252
    margin-bottom 0px
    text-align center
    font-family "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
    font-size 50px
    font-weight 500
#Main
    position relative
    // position absolute
    // float left
    height 100%
    width 100%
    margin-bottom 400px
    @media screen and (max-width: 800px) {
        height auto
        margin-bottom 100px
    }

.Main2
    // position absolute
    // float left
    height auto
    width 100%
    margin-top 100px
Icons made by <a href="https://www.flaticon.com/authors/freepik" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon"> www.flaticon.com</a>
#MenuBlock
    position relative
    // overflow hidden
    width 100%
    // float left
    // margin-top 0%
    height auto
    z-index 4

#BackToMenuButton
    z-index 4
    position fixed
    left 95%
    top 90%
    width 0%
    height 0%
    border-radius 50%
    box-shadow rgba(0, 0, 0, 0.5) 5px 5px
    background-image url(images/Down.png)
    background-size 100%

.textMargin
    position relative
    width auto
    margin 30px

#leftMain
    position relative
    height auto
    left 20%
    max-width 80%
    top 00%
    @media screen and (max-width: 1300px) {
        left 10%
        max-width 90%
    }
    @media screen and (max-width: 600px) {
        // display inline-block
        height auto
        left 0
        top 10px
        // margin 0 auto
    }
    @media screen and (max-width: 800px) {
        height auto
        top 15px
    }

#leftText
    position relative
    display inline-block
    height auto
    width 20%
    left 0%
    top 200px
    @media screen and (max-width: 850px) {
        width 100%
    }

#leftTextDiscrib
    position relative
    width 28%
    min-width 300px
    color #919191
    font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
    margin-top 15px
    font-size 1.22em
    @media screen and (max-width: 600px)
        width auto

#imgMain
    position relative
    width 60%
    height auto
    floar right
    margin-top 150px
    margin-left 150px
    margin-right 50px
    display inline-block
    @media screen and (max-width: 1150px) {
        width 50%
        margin-left 180px
        margin-right 20px
    }
    @media screen and (max-width: 850px) {
        margin-top 300px
        margin-left 0px
        width 100%
        height auto
    }

.MenuButton
    position relative
    height auto
    width 100px
    text-align center
    margin-top 0px
    background-repeat no-repeat
    background-size 60%
    border-radius 100%
    box-shadow 0px 0px 5px 0px

#DownloadButton
    position relative
    margin 10px
    height 50px
    width 200px
    text-align center
    vertical-align middle
    border-radius 50px 50px
    box-shadow rgba(145, 145, 145, 1) 5px 5px

#DownloadButtonText
    position relative
    height 100%
    width 100%
    padding-top 2%
    text-align center
    vertical-align middle
    color #FFFFFF
    font-size 2em
    font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
    font-weight bold

#TextBlock
    width 100%
    margin-top 0%
    text-align center
    color #ffffff
    font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
    font-size 3.5em
    font-weight bold
    z-index 10000000

@import url(http://fonts.googleapis.com/css?family=Roboto:700,400&subset=latin,cyrillic);
#Feature
    position relative
    height auto
    width 100%

#FeatureText
    position relative
    height auto
    width 42%
    min-width 450px
    text-align center
    margin auto
    margin-bottom 150px
    margin-top 50px
    color #525252
    font-weight 300
    font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
    font-size  2em
    @media screen and (max-width: 450px) {
        // display inline-block
        width 80%
        min-width 100px
        font-size 1.9em
        margin auto
    }
.AllAdvantages
    position relative
    margin-left 20%
    margin-right 10%
    margin-bottom 100px
    @media screen and (max-width: 1500px) {
        width 100%
        margin-left 0%
        margin-right 0%
    }
.Advantage
    position relative
    width 30%
    margin-bottom 30px
    margin-left 30px
    display inline-block
    @media screen and (max-width: 700px) {
        width 90%
        margin-left 10%
    }
.Advantages
    position relative
    width 80%
    margin-bottom 30px
    display inline-block
    img
        height 80px
        width 0px auto 20px
        margin-bottom 40px
    md-icon
        posititon relative
        height 80px
        width auto
        margin-bottom 50px
    strong
        width 100%
        display block
        font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
        font-weight 600
        font-size 22px
    p
        margin-top 20px
        font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
        font-size 18px
md-icon svg
    fill: inherit
.my-icon svg
{
   fill : #fff;
}
.iconAdvantege
    posititon relative
    height 80px
    width auto
    color #763DCA
    margin-bottom 20px
// .Advantage:hover
//     border-radius 20px
//     box-shadow 0px 0px 12px 3px #aaaaaa

#Topics
    z-index 1
    position relative
    height auto
    width 100%

.TopicBox
    position relative
    min-height 80%
    overflow hidden
    display inline-block
    width 25%
    margin 20px
    height auto
    border-radius 10px
    background-color #ffffff
    box-shadow rgba(145, 145, 145, 1) 10px 10px

.ImageBox
    width 200px
    height 200px
    margin-left 10%
    display block
    margin 10% auto

.TitleBox
    position relative
    width 100%
    height auto
    text-align center
    margin-top 10%
    color #763DCA
    font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
    font-size 25pt
    font-weight bold
.TextBox
    position relative
    width 80%
    text-align center
    height auto
    margin-top 10%
    margin-left 10%
    margin-right 10%
    color #525252
    font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
    font-size 20pt
    display inline-block
.TopicBox
    position relative
    width 27%
    min-width 410px
    height 740px
    min-height 70%
    overflow hidden
    margin-top 10%
    margin-right 3%
    margin-left 3%
    border-radius 10px
    background-color #ffffff
    box-shadow rgba(145, 145, 145, 1) 10px 10px
    @media screen and (max-width: 800px) {
        width 68%
        min-width 400px
        margin-right 16%
        margin-left 16%
        height 700px
        text-align center
        vertical-align middle
        min-width 100px
    }
    @media screen and (max-width: 450px) {
        width 88%
        height 650px
        min-width 100px
        margin-right 6%
        margin-left 6%
        min-width 100px
    }

#Task
    position relative
    height auto
    width 100%

#TaskButton
    position relative
    height auto
    width 100%
    float right
    transition 0.8s
    border: 2px solid #763DCA;
    border-radius 50px
    font-weight 550
    color #763DCA
    background-color #EEE0FB
#TaskButton:hover
    transition 0.8s
    opacity 0.7s
    border-radius 50px 50px
    color #ffffff
    background-color #763DCA
    box-shadow rgba(0, 0, 0, 0.75) 0px 0px 5px 0px

#TaskButtonText
    width auto
    height auto
    margin-left 20px
    margin-right 20px
    margin-top 10px
    margin-bottom 10px
    text-align center
    font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
    font-size 25pt
    font-weight bold

#TaskIn
    position relative
    height 60px
    width 100%
    float right
    border-style groove
    border-radius 50px
    border-width 3px
    font-size 30pt
    text-align center
    @media screen and (max-width: 1000px) {
        width 90%
        margin-left auto
        // display block
    }
.MainTask
    height auto
    width auto
    margin-top 100px
#TaskText
    position relative
    left 10%
    width 50%
    height auto
    margin-top 0px
    display inline-block
    margin-bottom 200px
    border-radius 50px
    background-color #ffffff
    box-shadow rgba(0, 0, 0, 0.5) 0px 0px 7px 0px
    @media screen and (max-width: 1100px) {
        width 90%
        left 5%
        margin-bottom 50px
        display block
    }

#rightTask
    width 300px
    hegith auto
    width 30%
    float right
    margin 5%
    @media screen and (max-width: 1100px) {
        float none
        width 70%
    }

#TextTask2
    position relative
    height auto
    width auto
    padding-top 100px
    padding-left 15%
    padding-right 15%
    padding-bottom 100px
    font-weight 800
    color #525252
    font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
    text-align center
    font-size 20pt
    @media screen and (max-width: 1100px) {
        width auto
        padding-top 10%
        padding-left 15%
        padding-right 15%
        padding-bottom 10%
        display block
    }

#TaskResultSucsessful
    z-index 2
    position absolute
    display none
    left 32.5%
    width 35%
    height 70%
    border-radius 50%
    background-image url(images/sucsessful.png)
    background-size 100%

#TaskResultnotSucsessful
    z-index 2
    position absolute
    display none
    left 32.5%
    width 35%
    height 70%
    border-radius 50%
    background-image url(images/notsucsessful.png)
    background-size 100%

#DownloadPlayMarket
    position relative
    height 200px
    width auto
    background: rgb(238,228,245);
    background: linear-gradient(90deg, rgba(238,228,245,1) 0%, rgba(238,186,235,1) 70%, rgba(159,158,231,1) 100%);
    border-radius 20px
    box-shadow rgba(0, 0, 0, 0.5) 0px 0px 5px 0px
    margin-top 100px
    margin-bottom 100px
    margin-left 20%
    margin-right 20%
    @media screen and (max-width: 1100px) {
        width 90%
        height 250px
        margin-right 5%
        margin-left 5%
    }
    @media screen and (max-width: 800px) {
        width 90%
        height 300px
        margin-right 5%
        margin-left 5%
    }

.imgFull
    position absolute
    height auto
    width auto
    float left
    background-size 100% 100%
    background-repeat no-repeat
.imgPlayMarket
    position: relative;
    height 100px
    width auto
    float right
    margin 50px 0
    margin-right 30px
    @media screen and (max-width: 1500px) {
        height 60px
        margin-right 10px
    }
    @media screen and (max-width: 700px) {
        width 80%
        height auto
        margin-left 10%
        float none
    }
.textPlayMarket
    position relative
    width 60%
    height 200px
    float left
    padding-top 60px
    margin-left 50px
    font-size 28px
    @media screen and (max-width: 1500px) {
        width 40%
        margin-left 20px
    }
    @media screen and (max-width: 700px) {
        width 80%
        margin-left 10%
        padding-top 20px
        height auto
        float none
        display block
    }
.DownloadText
    height 100%
    width 100%
    text-align center
    vertical-align middle
    color:#FFFFFF
    margin-top 8px
    margin-bottom 8px
    font-size 2em
    font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
    font-weight: bold

#GooglePlayBox
    position relative
    display inline-block
    width 27%
    min-width 400px
    height 760px
    margin-top 50px
    margin-bottom 50px
    margin-left 11%
    margin-right 11%
    background-repeat no-repeat
    background-size 100%
    background-image url("images/GooglePlay.jpg")
    border-radius 10px
    box-shadow rgba(0, 0, 0, 0.5) 10px 10px
    @media screen and (max-width: 800px) {
        width 60%
        margin-right 20%
        margin-left 20%
        height 700px
        text-align center
        vertical-align middle
        min-width 100px
    }
    @media screen and (max-width: 450px) {
        // display block
        width 80%
        height 540px
        min-width 100px
        margin-left 10%
        min-width 280px
        margin-right 10%
        // margin 0 auto
    }

#GooglePlay_DownloadButton
    position absolute
    left 45%
    top 86%
    height auto
    width 50%
    border-radius 50px 50px
    box-shadow rgba(0, 0, 0, 0.5) 0px 0px 15px
    color #64D597

#DownloadAPKBox
    position relative
    // top 10%
    display inline-block
    bottom 10%
    width 27%
    margin-top 50px
    margin-bottom 50px
    min-width 400px
    height 760px
    margin-left 11%
    margin-right 11%
    background-repeat no-repeat
    background-size 100%
    background-image url(images/GooglePlay.png)
    background-color #ffffff
    border-radius 10px
    box-shadow rgba(0, 0, 0, 0.50) 10px 10px
    @media screen and (max-width: 450px) {
        display none
        // height 640px
        // width 80%
        // margin-left 10%
        // margin-right 10%
        // min-width 100px
        // margin 0 auto
    }
    @media screen and (max-width: 800px) {
        display none
        // width 68%
        // min-width 400px
        // margin-right 16%
        // margin-left 16%
        // height 700px
        // text-align center
        // vertical-align middle
        // min-width 100px
    }

#DownloadAPK_DownloadButton
    position absolute
    left 45%
    top 86%
    height auto
    width 50%
    background #763DCA
    border-radius 50px 50px
    box-shadow rgba(0, 0, 0, 0.5) 0px 0px 15px
    color #763DCA

#AboutDevelopers
    position relative
    height auto
    width 100%

#finishImg
    position relative
    width auto
    width 40%
    margin-left 10%
    margin-top 120px
    display inline-block
    @media screen and (max-width: 1010px) {
        display none
    }

#finish
    position relative
    width 30%
    height auto
    display inline-block
    margin-top 300px
    float right
    margin-left 50px
    @media screen and (max-width: 1110px) {
        width 30%
        margin-top 200px
        margin-left 10%
        margin-right 10%
        margin-bottom 100px
    }
    @media screen and (max-width: 1010px) {
        width 80%
        margin-top 0px
        margin-left 10%
        margin-right 10%
        margin-bottom 100px
    }

#finishTitle
    height auto
    width auto
    color #763DCA
    font-weight 700
    font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
    font-size 25pt
    @media screen and (max-width: 1010px) {
        width 100%
        text-align center
    }

#finishText
    height auto
    width 70%
    margin-top 15px
    color #919191
    font-weight:500
    font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
    font-size 17pt
    @media screen and (max-width: 1020px) {
        width 100%
        text-align center
    }
    @media screen and (max-width: 480px) {
        width 100%
        margin-left 0%
        margin-right 0%
        text-align center
    }

#AboutUs
    position relative
    height auto
    width 100%

#headerAboutUs
    position relative
    height 100%
    width 100%
    text-align center
    vertical-align middle
    color:#FFFFFF
    font-size 3.6em
    font-family: "Euclid Circular A",-apple-system,BlinkMacSystemFont,Roboto,Helvetica,Arial,"Apple Color Emoji",sans-serif
    font-weight: bold

#Media
    position relative
    margin 0px 0px 0px 0px auto
    text-align center
    vertical-align middle
    margin-top 40px

#social
    height auto
    width 150px
    margin 60px
    // margin-left 20%
    transition 1.0s
    margin-bottom 150px
    display inline-block
    @media screen and (max-width: 750px) {
        height 100px
        width 100px
    }
    @media screen and (max-width: 600px) {
        height 50px
        width 50px
    }
#social:hover
    transition 0.8s
    width 200px
#telegram
    position relative
    height 200px
    width 200px
    margin-bottom 50px
    margin-left 80px
    display inline-block
    background-repeat no-repeat
    border-radius 50%
    background-image url(images/telegram.png)
    background-size 100% 100%
    background-color #ffffff
    box-shadow rgba(0, 0, 0, 0.5) 10px 10px
    @media screen and (max-width: 450px) {
        height 100px
        width 100px
    }

.gradient
    z-index 3
    background linear-gradient(to left, #763DCA, #763DCA)

.gradient2
    z-index 3
    background linear-gradient(to left, #26de81, #26de81)

body
    margin 0px 0px
    overflow-x hidden

#design1
    position absolute
    left 80%
    width 20%
    height 40%
    border-radius 50%

#design2
    position absolute
    top 10%
    left 60%
    width 20%
    height 20%
    background-color #ffffff
    border-radius 50%

#design3
    position relative
    width 100%
    height 100px
    border-top-right-radius 100%
    border-top-left-radius 90%
    @media screen and (max-width: 1100px) {
        margin-top 100px
    }

#designBottom1
    position relative
    width 100%
    height 10%
    z-index 4
    top 90%
    z-index 4
    border-top-right-radius 100%
    border-top-left-radius 90%

#design4
    position relative
    width 100%
    height 100px
    border-bottom-right-radius 100%

#design5
    position relative
    width 100%
    height 100px
    border-top-left-radius 100%

#design6
    position relative
    width 100%
    height 100px
    border-bottom-left-radius 100%
    border-bottom-right-radius 100%

#design7
    position absolute
    // top 90%
    width 100%
    height 10%
    border-top-left-radius 100%

#design8
    position absolute
    width 100%
    height 10%
    top 90%
    border-top-right-radius 100%
    border-top-left-radius 90%

</style>
