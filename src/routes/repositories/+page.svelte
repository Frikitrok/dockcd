<script lang="ts">
  import Repo from './Repo.svelte';
  import AddRepo from './AddRepo.svelte';
</script>

<div class="content_wrapper">
  <div class="add_repo_wrap">
    <AddRepo/>
  </div>
  <div>
    <Repo/>
  </div>
</div>

<style>
  .content_wrapper {
    float: left;
    padding: 25px;
    width: calc(100% - 250px);
  }

  .add_repo_wrap {
    margin-bottom: 20px;
  }
</style>