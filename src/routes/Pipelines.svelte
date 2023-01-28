<DataTable table$aria-label="Pipelines list" style="width: 100%;">
  <Head>
    <Row>
      <Cell>Pipeline name</Cell>
      <Cell>Schema</Cell>
      <Cell>Status</Cell>
    </Row>
  </Head>
  <Body>
    <Row>
      <Cell>Backend</Cell>
      <Cell>Backend</Cell>
      <Cell>Finished</Cell>
    </Row>
    <Row>
      <Cell>Redis</Cell>
      <Cell>Database</Cell>
      <Cell>In progress</Cell>
    </Row>
    <Row>
      <Cell>Internal services</Cell>
      <Cell>Multi-service</Cell>
      <Cell>Finished</Cell>
    </Row>
    <Row>
      <Cell>Monitoring</Cell>
      <Cell>Multi-service</Cell>
      <Cell>Finished</Cell>
    </Row>
  </Body>
</DataTable>

<script lang="ts">
  import DataTable, { Head, Body, Row, Cell } from '@smui/data-table';
</script>
