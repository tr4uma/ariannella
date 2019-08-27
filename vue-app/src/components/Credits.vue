<template>
  <div class="credits">
    <div class="items">
      <div class="item">
        <span>
          <font-awesome-icon
            :icon="github"
            size="2x"
          ></font-awesome-icon><a href="https://github.com/tr4uma">github.com/tr4uma</a>
        </span>
        <span>
          <font-awesome-icon
            :icon="instagram"
            size="2x"
          ></font-awesome-icon><a href="https://www.instagram.com/traumatizzato/">@traumatizzato</a>
        </span>
      </div>
      <div class="item">
        © Copyright 2019 - ariannella - All rights reserved
      </div>
    </div>
  </div>
</template>

<script>

import { library } from '@fortawesome/fontawesome-svg-core'
import { faGithub, faInstagram } from '@fortawesome/free-brands-svg-icons'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

library.add(faGithub, faInstagram)

export default {
  name: 'Credits',
  data () {
    return {
      github: faGithub,
      instagram: faInstagram
    }
  },
  components: {
    FontAwesomeIcon
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
* {
  font-size: 0.8rem;
}
a {
  padding-left: 0.2rem;
}
span {
  padding: 0.1rem;
  display: flex;
  align-items: center;
}
.credits {
  display: flex;
  flex-direction: column;
  flex: 1;
  justify-content: center;
  justify-items: center;
}
.items {
  display: flex;
  flex-direction: row;
  flex: 1;
  justify-content: center;
  justify-items: center;
}
.item {
  display: flex;
  flex: 1;
  flex-direction: column;
  justify-content: center;
  justify-items: center;
  align-items: center;
}
</style>
