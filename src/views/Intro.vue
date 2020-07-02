<template>
  <div class="home">
    <img alt="Vue logo" src="https://res.cloudinary.com/dr26yn9mp/image/upload/v1593723183/WhatsApp_Image_2020-07-01_at_1.19.55_PM_slnl2p.jpg">
    <TechTalk title="Bem vindos a Tech Talk Globalsys"/>
  </div>
</template>

<script>
// @ is an alias to /src
import TechTalk from '@/components/TechTalk.vue'

export default {
  name: 'Home',
  components: {
    TechTalk
  }
}
</script>
