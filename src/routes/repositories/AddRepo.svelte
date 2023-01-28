<Dialog
  bind:open
  aria-labelledby="simple-title"
  aria-describedby="simple-content"
>
  <!-- Title cannot contain leading whitespace due to mdc-typography-baseline-top() -->
  <Title id="simple-title" style="width: 500px; text-align: center;">Fill new repository</Title>

  <div class="margins">
    <Textfield bind:value={valueA} label="Repository name" style="width: 100%;">
      <HelperText slot="helper">Name of created repository</HelperText>
    </Textfield>
  </div>
  <div class="margins">
    <Textfield bind:value={valueB} label="Repository url" style="width: 100%;">
      <HelperText slot="helper">Link of repository API</HelperText>
    </Textfield>
  </div>

  <div class="segment_wrapper">
  <SegmentedButton segments={choices} let:segment singleSelect bind:selected style="width: 100%">
    <!-- Note: the `segment` property is required! -->
    <Segment style="width: 33.3%; text-align: center;" {segment}>
      <Label>{segment}</Label>
    </Segment>
  </SegmentedButton>
  </div>

  <Actions style="display: block; float: left; padding: 40px; margin-bottom: 10px;">
    <Button on:click={() => (clicked = 'No')}>
      <Label>Add</Label>
    </Button>
    <Button on:click={() => (clicked = 'Yes')}>
      <Label>Cancel</Label>
    </Button>
  </Actions>
</Dialog>

<Button on:click={() => (open = true)} style="width: 100%; border: 1px solid grey;">
  <Label>Add new repository</Label>
</Button>

<script lang="ts">
  import Dialog, { Title, Content, Actions } from '@smui/dialog';
  import Button, { Label } from '@smui/button';
  import Textfield from '@smui/textfield';
  import HelperText from '@smui/textfield/helper-text';
  import SegmentedButton, { Segment } from '@smui/segmented-button';

  let focused = false;
  let valueA = '';
  let valueB = '';
  let open = false;
  let clicked = 'Nothing yet.';
  let choices = ['ECR', 'GCP', 'Docker'];
  let selected = 'Docker';
</script>

<style>
  .margins {
    margin: 10px 0;
    float: left;
    width: calc(100% - 80px);
    padding: 0 40px;
  }

  .segment_wrapper {
    width: calc(100% - 80px);
    padding: 0 40px;
    margin-bottom: 20px;
  }
</style>