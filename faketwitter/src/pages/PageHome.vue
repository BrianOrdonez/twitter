<template>
  <q-page>
    <div class="q-py-lg q-px-md row items-end q-col-gutter-md">
      <div class="col">
        <q-input
          class="new-tweet"
          bottom-slots
          v-model="newcontent"
          placeholder="What's Up"
          counter
          maxlength="280"
          :dense="dense"
          autogrow
        >
          <template v-slot:before>
            <q-avatar size="xl">
              <img src="https://cdn.quasar.dev/img/avatar5.jpg" />
            </q-avatar>
          </template>
        </q-input>
      </div>
      <div class="col col-shrink">
        <q-btn
          :disable="!newcontent"
          class="q-mb-lg"
          unelevated
          no-caps
          rounded
          color="primary"
          label="Unelevated Rounded"
        />
      </div>
    </div>

    <q-separator class="divider" size="10px" color="grey-2" />
    <q-list>
      <q-item clickable v-ripple class="q-py-md">
        <q-item-section avatar top>
          <q-avatar>
            <img src="https://cdn.quasar.dev/img/avatar5.jpg" />
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label class="text-subtitle1">
            <strong> Jane Doe </strong>
            <span class="text-grey-7"> @random_username123 </span>
          </q-item-label>
          <q-item-label class="new-content text-body!">
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
            aliquip ex ea commodo consequat. Duis aute irure dolor in
            reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
            pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
            culpa qui officia deserunt mollit anim id est laborum."
          </q-item-label>
          <div class="q-icons">
            <q-btn flat round color="grey" icon="far fa-comment" />
            <q-btn flat round color="grey" icon="fas fa-retweet" />
            <q-btn flat round color="grey" icon="far fa-heart" />
            <q-btn flat round color="grey" icon="fas fa-trash" />
          </div>
        </q-item-section>

        <q-item-section side top> 1 min ago </q-item-section>
      </q-item>
    </q-list>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "PageHome",
  data() {
    return { newcontent: "" };
  },
});
</script>

<style lang="sass">
.new-tweet
  textarea
  font-size: 19px
  line-height: 1.4

  .divider

    border-top: 100px solid
    border-bottom: 100px solid
    border-color: $red

    .new-content
      white-space: pre-line

      .q-icons
        margin-left: -131px
</style>
