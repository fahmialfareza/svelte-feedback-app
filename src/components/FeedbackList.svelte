<script>
  // import { onDestroy, onMount } from "svelte";
  import { fade, scale } from "svelte/transition";
  import FeedbackItem from "./FeedbackItem.svelte";
  import { FeedbackStore } from "../stores";

  // let feedback = [];

  // const unsubsribe = FeedbackStore.subscribe((data) => (feedback = data));

  // onMount(() => {});

  // onDestroy(() => {
  //   unsubsribe();
  // });
</script>

{#each $FeedbackStore as fb (fb.id)}
  <div in:scale out:fade={{ duration: 500 }}>
    <FeedbackItem item={fb} />
  </div>
{/each}
