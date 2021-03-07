<form class="messageComposer">
  <textarea class="messageComposer__textarea">message composer</textarea>
  <button class="messageComposer__submit" type="submit">submit</button>
</form>

<style lang="scss">
  @import "../../styles/variables";

  .messageComposer {
    padding: 0.5rem;
    display: flex;
    align-items: stretch;

    &__textarea {
      flex-grow: 1;
      overflow: hidden;
      margin: 0 1rem 0 0;
      padding: 0.5rem;
      height: 2rem;
      border: 1px solid $color-border-gray;
      resize: none;
      line-height: 1;
      font-size: 1rem;
    }

    &__submit {
      margin: 0;
    }
  }
</style>
