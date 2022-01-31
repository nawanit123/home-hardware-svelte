<script>
  import { onMount } from 'svelte';
  import NavigationBar from './components/NavigationBar.svelte';

  let data;
  onMount(async () => {
    const client = contentful.createClient({
      space: '9jo7ly0kaj2i',
      accessToken: '6cjsFFuJF9j3g1xD1jy8FhDEzvy8v_oL9oSSFrlJHyo'
    });
    console.log(client);

    client
      .getEntry('43s8eOA2aUGusOmLX5229J')
      .then(res => {
        data = res.fields.bannerHeader;
        console.log(data);
      })
      .catch(console.log);
  });
</script>

<main>
  <NavigationBar />
</main>

<style>
</style>
