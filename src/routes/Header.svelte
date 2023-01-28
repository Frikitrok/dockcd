<div class="flexy">
  <div class="top-app-bar-container flexor">
    <TopAppBar
      variant="static"
      {prominent}
      {dense}
      color={secondaryColor ? 'secondary' : 'primary'}
    >
      <Row>
        <Section>
          <IconButton class="material-icons" on:click={() => sidebar = !sidebar}>menu</IconButton>
          <Title>DockCD.io</Title>
        </Section>
        <Section align="end" toolbar>
          <IconButton class="material-icons" aria-label="Download"
            >file_download</IconButton
          >
          <IconButton class="material-icons" aria-label="Print this page"
            >print</IconButton
          >
          <IconButton class="material-icons" aria-label="Bookmark this page"
            >bookmark</IconButton
          >
        </Section>
      </Row>
    </TopAppBar>
  </div>
</div>

<script lang="ts">
  import TopAppBar, { Row, Section, Title } from '@smui/top-app-bar';
  import IconButton from '@smui/icon-button';
  import Checkbox from '@smui/checkbox';
  import FormField from '@smui/form-field';

  let prominent = false;
  let dense = false;
  let secondaryColor = false;
  export let sidebar = false;
</script>

<style>
  .top-app-bar-container {
    max-width: 100%;
    width: 100%;
    height: 64px;
    /* border: 1px solid
      var(--mdc-theme-text-hint-on-background, rgba(0, 0, 0, 0.1)); */
    margin: 0px;
    background-color: var(--mdc-theme-background);

    overflow: auto;
    display: inline-block;
  }

  @media (max-width: 480px) {
    .top-app-bar-container {
      margin-right: 0;
    }
  }

  .flexy {
    display: flex;
    flex-wrap: wrap;
  }

  .flexor {
    display: inline-flex;
    flex-direction: column;
  }

  /* .flexor-content {
    flex-basis: 0;
    height: 0;
    flex-grow: 1;
    overflow: auto;
  } */
</style>