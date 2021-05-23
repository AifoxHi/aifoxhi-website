<script setup lang="ts">
import { ref } from 'vue'
import { useRouter } from 'vue-router'
import { useI18n } from 'vue-i18n'
import { isDark, toggleDark } from '~/logic'

const name = ref('')

const router = useRouter()
const go = () => {
  if (name.value)
    router.push(`/hi/${encodeURIComponent(name.value)}`)
}

const { t } = useI18n()
</script>

<template>
<div class="legacy_style" style="display:none;">
  <p style="display:none;">古いブラウザ？ 私は1996年から1990年にかけて? <br> Old browser? between 1996-1990? <br> Debug Info: Browser don't support any CSS!</p>
  <a href="veryold" style="display:none;">--&gt;*リンク | Link*&lt;--</a>
 </div> 
  <div id="ie6">
    <p>古いブラウザ？ 私は2011年から1996年にかけて? <br> Old browser? between 2011-1996? <br> Debug Info: You using IE6&lt;/Trident/MSHTML</p>
    <a href="old">--&gt;*リンク | Link*&lt;--</a>
  </div>
<div class="ie10plus-notice"><p>古いブラウザ？ 私は2008年から1996年にかけて? <br> Old browser? between 2008-1996? <br> Debug Info: Browser is IE10>/Trident/MSHTML/Chakra/EdgeHTML and Microsoft Edge Legacy (Only up to 18) . Please note that Edge Legacy were updated up to 2020 year and some other browsers such as Mahathon still use it, in that case change browser or just ignore this message.</p><br><a c href="old">--&gt;*リンク | Link*&lt;--</a></div>
  <div>
    <p class="text-4xl">
      <fxemoji:foxheart class="inline-block" />
    </p>
    <p>
      <a rel="noreferrer" href="https://aifoxhi.tk" target="_blank">
        AifoxHi {{ t('links.site') }}
      </a>
    </p>
    <p>
      <em class="text-sm opacity-75">{{ t('intro.desc') }}</em>
    </p>

    <div class="py-2" />
    <a class="row aikon-button" title="Twitter Account" href="http://blog.aifoxhi.tk/">
      <div class="column difleft"><p class="text-5xl"><mdi:feather /><span>JP</span></p></div>
      <div class="column difright center-text">Livedoor Blog (Japan 日本国 ジャパン)</div>
    </a>
    <a class="row aikon-button" title="Twitter Account" href="https://twitter.com/aifoxhi">
      <div class="column difleft"><p class="text-5xl"><bytesize:twitter /><span>JP</span></p></div>
      <div class="column difright center-text">Twitter: @AifoxHi</div>
    </a>
    <a class="row aikon-button" title="Instagram Profile" href="https://instagram.com/aifoxhi">
      <div class="column difleft"><p class="text-5xl"><mdi:instagram /><span class="multilang">EN</span><span>JP</span></p></div>
      <div class="column difright center-text">Instagram: @AifoxHi</div>
    </a>
    <a class="row aikon-button" title="YouTube Channel" href="https://www.youtube.com/channel/UCOf--8ruux6bMa8p2CjgoNQ">
      <div class="column difleft"><p class="text-5xl"><carbon:logo-youtube /><span>JP</span></p></div>
      <div class="column difright center-text">YouTube: AifoxHi Japan 日本国 ジャパン</div>
    </a>
    <a class="row aikon-button" title="Twitter Page" href="https://www.youtube.com/channel/UCL4Txuua4Bfb_baf-gpR2mQ">
      <div class="column difleft"><p class="text-5xl"><carbon:logo-youtube /><span>EN</span></p></div>
      <div class="column difright center-text">AifoxHi English / International</div>
    </a>
  </div>
</template>

<route lang="yaml">
meta:
  layout: home
</route>
