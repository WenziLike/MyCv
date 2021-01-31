<template>
  <div class="wrapper-content">
    <h1 class="wrapper-title">{{ firstName }} {{ lastName }}</h1>
    <div class="wapper-content flex-sa">
      <div class="card">
        <section>
          <div class="card shadow-drop-2-center">
            <div class="wrapper-logo">
              <strong>{{ logo }}</strong>
            </div>
            <div class="card">
              <img
                src="./../assets/myfoto.jpg"
                class="circle-image"
                alt="Viacheslav Murakhin"
              />
            </div>
            <ul class="card-contacts">
              <li v-for="item in contacts" :key="item">
                <a :href="item.href">{{ item.text }}</a>
              </li>
              <!-- <li>
                <strong>tel:</strong>
                <a href="tel:+48537886161"
                  ><strong> +48 537 88 61 61</strong>
                </a>
              </li>
              <li>
                <strong>email:</strong>
                <a href="mailto:SlavaMyraxin@icloud.com"
                  ><strong> SlavaMyraxin@icloud.com</strong>
                </a>
              </li>
              <li>
                <strong>Skype:</strong>
                <a href="callto:skype:live:.cid.f00786ab772de349"
                  ><strong> Skype</strong>
                </a>
              </li> -->
            </ul>
            <div class="card-adress">
              <p>31-425 Kraków, Poland</p>
              <p>Rogatka 7</p>
            </div>
          </div>
        </section>
        <!-- ============ -->
        <app-general-all-skills></app-general-all-skills>
      </div>
      <!-- ============ -->
      <app-general-content></app-general-content>
    </div>
    <!-- ============ -->
    <button class="btn" type="submit">View Certificates</button>
    <div class="footer card br-5">
      <section>
        <strong v-html="copy"></strong>
        <strong>VMurakhin, 2021</strong>
      </section>
    </div>
  </div>
</template>

<script>
import AppGeneralContent from '@/components/AppGeneralContent'
import AppGeneralAllSkills from '@/components/AppGeneralAllSkills'

export default {
  inject: ['logo', 'copy', 'firstName', 'lastName', 'contacts'],
  components: { AppGeneralContent, AppGeneralAllSkills }
}
</script>

<style lang="scss" scoped>
</style>