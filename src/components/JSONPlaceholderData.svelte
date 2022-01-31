<script>
  import { onMount } from 'svelte';

  let jsonPlaceHolderData;

  let postTitle, postBody, postId;
  onMount(async () => {
    const res = await fetch('https://jsonplaceholder.typicode.com/posts/1');
    jsonPlaceHolderData = await res.json();
    postTitle = jsonPlaceHolderData.title;
    postBody = jsonPlaceHolderData.body;
    postId = jsonPlaceHolderData.id;
  });
</script>

<div class="JSONPlaceHolder">
  <h3>{postTitle}</h3>
  <p>{postBody}</p>
</div>
