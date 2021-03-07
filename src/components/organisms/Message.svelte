<script lang="ts">
  import DefaultAvatarFemale from "../atoms/DefaultAvatarFemale.svelte";
</script>

<article class="message">
  <div class="message__avatarContainer">
    <div class="message__avatar">
      <DefaultAvatarFemale />
    </div>
  </div>
  <div class="message__contentContainer">
    <header class="message__header">
      <h1 class="message__username">
        <a class="message__usernameLink" href="#">Abcd Efghijk</a>
      </h1>
      <time class="message__time">12:34 PM</time>
    </header>
    <div class="message__content">
      音声SNS「クラブハウス」を活用する企業が続々と登場しています。どんな狙いがあるのでしょうか？<br
      />沖縄県石垣島で創業70年の泡盛メーカーを営む池原酒造。新型コロナで自慢の泡盛「白百合」の売り上げも減少してしまいました。そんななか、社長が始めたのは音声SNS「クラブハウス」です。<br
      />池原酒造代表取締役社長・池原優さん：「Clubhouseを使用したきっかけですが、本当、最初は興味本位という感じでした。例えば、大手広告店、お笑い芸人、アーティストとか、議員とか、皆、真剣にアドバイスしてくれた」<br
      />話手が増えれば、聞く人も増える。その連鎖は、同じ沖縄の仲間をも引き寄せました。伝統的な染物「琉球びんがた」の職人・知念冬馬さんも会話に参加し、話は思わぬ方向に進みました。
    </div>
  </div>
</article>

<style lang="scss">
  @import "functions";
  @import "variables";

  .message {
    display: flex;
    padding: 0.5rem 1.25rem;

    &:hover {
      background-color: $color-bg-lightGray;
    }

    &__avatarContainer {
      flex-shrink: 1;
      margin-right: 0.5rem;
    }

    &__avatar {
      overflow: hidden;
      width: 2.25rem;
      height: 2.25rem;
      border-radius: 4px;
    }

    &__contentContainer {
      flex-grow: 1;
    }

    &__header {
      display: flex;
      margin-bottom: 0.25rem;
      align-items: center;
    }

    &__username {
      margin: 0 0.5rem 0 0;
      font-size: px2rem(15);
      font-weight: 900;
    }

    &__usernameLink {
      color: #000;
    }

    &__time {
      font-size: 0.75rem;
      color: $color-text-gray;
    }

    &__content {
      box-sizing: border-box;
      font-size: px2rem(15);
      font-variant-ligatures: common-ligatures;
      font-weight: 400;
      line-height: px2rem(22);
      overflow-wrap: break-word;
      text-align: left;
      user-select: text;
      -webkit-font-smoothing: antialiased;
    }
  }
</style>
