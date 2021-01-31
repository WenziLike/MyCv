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
            <div class="circle-image"></div>
            <ul class="card-contacts">
              <li v-for="item in contacts" :key="item">
                <a :href="item.href">{{ item.text }}</a>
              </li>
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
#app {
  .btn {
    position: absolute;
    bottom: 6%;
    right: 4%;
    text-align: right;
    font-size: 1rem;
    font-weight: 600;
    text-transform: uppercase;
    height: 50px;
    min-width: 120px;
    padding: 10px;
    border-radius: 5px;
    border: none;
    outline: none;
    cursor: pointer;
    background: #dde1e7;
    color: #3498db;
    box-shadow: 4px 5px 10px #707070b2, 2px 2px 5px rgba(94, 104, 121, 0.288);
    &:active {
      box-shadow: -3px -3px 7px #ffffff73, 2px 2px 5px rgba(94, 104, 121, 0.288);
      color: #2c3e50;
      text-align: left;
    }
  }
  .circle-image {
    width: 300px;
    height: 300px; /* Ширина и высота */
    border-radius: 50%; /* Превращаем в круг */
    background: url("./../assets/myfoto.jpg") no-repeat -50px 0; /* Параметры фона */
    background-size: auto 400px; /* Высота фотографии равна высоте элемента */
    box-shadow: 2px 6px 12px rgba(0, 0, 0, 0.2);
  }
}
</style>