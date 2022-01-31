<script>
  import { onMount } from 'svelte';

  let jsonPlaceHolderData;
  let firstPost;
  let postTitle, postBody, postId;
  onMount(async () => {
    const res = await fetch('https://jsonplaceholder.typicode.com/posts/1');
    jsonPlaceHolderData = await res.json();
    firstPost = jsonPlaceHolderData[0];
    postTitle = firstPost.title;
    postBody = firstPost.body;
    postId = firstPost.id;
  });
</script>

<div class="JSONPlaceHolder">
  <h3>{postTitle}</h3>
  <p>{postBody}</p>
</div>
