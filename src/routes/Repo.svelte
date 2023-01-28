<DataTable table$aria-label="Repo list" style="width: 100%;">
  <Head>
    <Row>
      <Cell>Repository name</Cell>
      <Cell>Type</Cell>
      <Cell>Status</Cell>
    </Row>
  </Head>
  <Body>
    <Row>
      <Cell>Service-1</Cell>
      <Cell>ECR</Cell>
      <Cell>Green</Cell>
    </Row>
    <Row>
      <Cell>Service-2</Cell>
      <Cell>ECR</Cell>
      <Cell>Red</Cell>
    </Row>
    <Row>
      <Cell>Service-3</Cell>
      <Cell>GCP</Cell>
      <Cell>Green</Cell>
    </Row>
    <Row>
      <Cell>Terraform</Cell>
      <Cell>Docker</Cell>
      <Cell>Red</Cell>
    </Row>
  </Body>
</DataTable>

<script lang="ts">
  import DataTable, { Head, Body, Row, Cell } from '@smui/data-table';
</script>
