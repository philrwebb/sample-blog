<script context="module">
   import { findPost } from '../../posts';
   export function preload(page) {
      console.log(page);
      return { post : findPost(page.params.permalink.substring(1)) };
   }
</script>

<script>
   export let post;
</script>

<h1>{post.title}</h1>

{@html post.html}
