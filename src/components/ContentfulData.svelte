<script>
  import { onMount } from 'svelte';

  let contentfulData;
  onMount(async () => {
    const client = contentful.createClient({
      space: '9jo7ly0kaj2i',
      accessToken: '6cjsFFuJF9j3g1xD1jy8FhDEzvy8v_oL9oSSFrlJHyo'
    });
    console.log(client);

    client
      .getEntry('43s8eOA2aUGusOmLX5229J')
      .then(res => {
        contentfulData = res.fields.bannerHeader;
      })
      .catch(console.log);
  });
</script>

<div class="ContentfulData">
  <p>{contentfulData}</p>
</div>
