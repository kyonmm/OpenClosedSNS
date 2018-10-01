<template>
  <div class="thread">
      <article class="media">
      <figure class="media-left icon">
          <p class="image is-64x64">
              <img class="user-image" src="favicon.ico"/>
          </p>
      </figure>
      <div class="media-content">
          <div class="content">
      <span class="screen-name"><strong>sample</strong></span>
      <span class="time-lapsed"><small>3h</small></span>
      <span class="reactions"/>
      <span class="description thread-start">
          {{threadStart}}
    </span>
      <ol>
        <li v-for="comment in comments">
            <div class="comment">
                {{comment}}
            </div>
        </li>
      </ol>
      </div>
      </div>
      </article>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class Thread extends Vue {
  @Prop() private threadStart!: string;
  @Prop() private comments!: string[];
}
</script>

<style scoped lang="scss">
</style>