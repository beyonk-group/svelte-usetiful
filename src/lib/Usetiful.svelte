<script>
  export let token
  export let tags = {}

  const url = 'https://www.usetiful.com/dist/usetiful.js'

  function usetiful (node, tags) {
    window.usetifulTags = tags
    const script = document.createElement('script')
    script.async = true
    script.src = url
    script.setAttribute('id', 'usetifulScript')
    script.dataset.token = token
    document.head.appendChild(script)

    return {
      update (tags) {
        window.usetifulTags = tags
      },
      destroy () {
        document.head.removeChild(script)
        delete window.usetifulTags
      }
    }
  }
</script>

<span class:configured={!!token} use:usetiful={tags}>
  Usetiful is missing required property "token". Please see the documentation.
</span>

<style>
  span.configured {
    position: absolute;
    top: -999px;
    left: -999px;
    color: transparent;
  }
</style>
