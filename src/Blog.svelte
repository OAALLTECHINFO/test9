<script>
  import { Router, Route, Link } from "svelte-navigator";
  export let blogRoute;
</script>

<div class="Blog">
  <h2>Blog</h2>
  <span>You're at blog</span>
  <nav>
    <Link to="../">Go back to the landing page</Link>
  </nav>
</div>
