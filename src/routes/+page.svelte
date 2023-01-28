<script lang="ts">
  import Repo from './Repo.svelte';
  import Pipelines from './Pipelines.svelte';
</script>

<div class="content_wrapper">
  <Repo/>
  <br>
  <br>
  <br>
  <div class="pipelines">
    <Pipelines/>
  </div>
  <div class="pipe_img">
    <center><img src="/PieChart.svg"></center>
  </div>
</div>

<style>
  .content_wrapper {
    float: left;
    padding: 25px;
    width: calc(100% - 250px);
  }

  .pipelines {
    width: calc(100% - 400px);
    float: left;
  }

  .pipe_img {
    width: 400px;
    float: left;
  }

  .pipe_img img {
    width: 250px;
  }
</style>