<script>
  import { Page, Navbar, Block, List, ListItem } from 'framework7-svelte';

  const effects = [
    'f7-circle',
    'f7-cover',
    'f7-cover-v',
    'f7-dive',
    'f7-fade',
    'f7-flip',
    'f7-parallax',
    'f7-push',
  ];
</script>

<Page>
  <Navbar title="Page Transitions" backLink="Back" />

  <Block strong>
    <p>
      In addition to default theme-specific page transition it is possible to create custom page
      transition or use one of the additional transition effects:
    </p>
  </Block>

  <List>
    {#each effects as effect}
      <ListItem link={`/page-transitions/${effect}/`} title={effect} transition={effect} />
    {/each}
  </List>
</Page>
