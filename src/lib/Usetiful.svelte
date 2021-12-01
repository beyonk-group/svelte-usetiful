<script>
  export let token
  export let segment
  export let language
  export let role
  export let firstName

  const url = 'https://www.usetiful.com/dist/usetiful.js'

  $: config = {
    ...segment && { segment },
    ...language && { language },
    ...role && { role },
    ...firstName && { firstName },
  }

  function useitful (node, config) {
    window.useitfulTags = config
    const script = document.createElement('script')
    script.async = true
    script.src = url
    script.setAttribute('id', 'usetifulScript')
    script.dataset.token = token
    document.head.appendChild(script)

    return {
      destroy () {
        document.head.removeChild(script)
        delete window.useitfulTags
      }
    }
  }
</script>

<span class:configured={!!token} use:useitful={config}>
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
