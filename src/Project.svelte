<script>
  export let name;
  export let url;
</script>

<style>
  li {
    list-style-type: none;
    font-size: 15px;
    margin-bottom: 10px;
    padding: 8px 20px;
    background-color: #323330;
    color: azure;
    text-transform: uppercase;
  }
  @media only screen and (min-width: 600px) {
    li {
      font-size: 20px;
    }
  }
</style>

<li>
  <a href={url} target="_blank">{name}</a>
</li>
