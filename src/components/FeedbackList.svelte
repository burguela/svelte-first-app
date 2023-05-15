<script lang="ts">
  import {fade,scale} from 'svelte/transition'
  import FeedbackItem from './FeedbackItem.svelte';
  import { FeedbackStore } from '../stores/stores';

</script>

{#each $FeedbackStore as fb (fb.id)}
  <div in:scale out:fade="{{duration: 500}}">
    <FeedbackItem item={fb} />
  </div>
{/each}