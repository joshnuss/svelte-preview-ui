<script>
  import Screen from './Screen.svelte'

  export let address = "https://google.com"
</script>

<Screen>
  <div class="address-bar" slot="bar">
    <input value={address}/>
  </div>

  <slot/>
</Screen>

<style>
  .address-bar {
    display: flex;
    padding: 3px;
    margin: 5px 5px 5px 100px;
  }
  .address-bar input {
    background: var(--screen-shadow-color);
    border: none;
    padding: 0.2rem 1rem;
    border-radius: 15px;
    font-size: 1.2rem;
    display: block;
    width: 100%;
  }
</style>
