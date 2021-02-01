<template>
  <div class="container">
    <div class="wrapper">
      <div class="wrapper-social">
        <ul>
          <li>
            <a href="https://www.facebook.com/WenziLike/" target="_blank"
              >facebook</a
            >
          </li>
          <li>
            <a href="https://t.me/Like_Slawomir" target="_blank">Telegram</a>
          </li>
          <li>
            <a href="https://github.com/WenziLike" target="_blank">Git</a>
          </li>
        </ul>
      </div>
      <!-- =================================  General-->
      <app-general-cv></app-general-cv>
    </div>
  </div>
</template>

<script>
import dataFile from '@/dataFile'
import AppGeneralCv from '@/components/AppGeneralCv'

export default {
  components: { AppGeneralCv },
  data() {
    return {
      logo: '<VM />',
      copy: '&#169',
      checkMark: '&#10003;',
      year: ''
    }
  },
  methods: {
    // year() {
    //   // this.year = new Data().
    // }
  },
  provide() {
    return {
      checkMark: this.checkMark,
      copy: this.copy,
      logo: this.logo,
      firstName: dataFile.firstName,
      lastName: dataFile.lastName,
      contacts: dataFile.contacts,
      skills: dataFile.skills,
      education: dataFile.education,
      languages: dataFile.languages,
      positionName: dataFile.positionName,
      whatAreSearchingFor: dataFile.whatAreSearchingFor,
      jobObjective: dataFile.jobObjective,
      otherActivities: dataFile.otherActivities
    }
  }
}
</script>