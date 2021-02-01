<template>
  <div class="container">
    <div class="wrapper">
      <div class="wrapper-social">
        <ul>
          <li v-for="item in social" :key="item">
            <a :href="item.link" target="_blank">{{ item.text }}</a>
          </li>
        </ul>
      </div>
      <app-general-cv></app-general-cv>
      <button class="btn" @click="modal = true">View Certificates</button>
    </div>
  </div>
  <teleport to="body">
    <app-modal v-if="modal" @close="modal = false"></app-modal>
  </teleport>
</template>

<script>
import dataFile from '@/dataFile'
import AppGeneralCv from '@/components/AppGeneralCv'
import AppModal from '@/components/AppModal'

export default {
  components: { AppGeneralCv, AppModal },
  data() {
    return {
      logo: '<VM />',
      copy: '&#169',
      checkMark: '&#10003;',
      social: dataFile.social,
      modal: false
    }
  },
  provide() {
    return {
      checkMark: this.checkMark,
      copy: this.copy,
      logo: this.logo,
      firstName: dataFile.firstName,
      lastName: dataFile.lastName,
      contacts: dataFile.contacts,
      adress: dataFile.adress,
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

<style lang="scss" scoped>
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
</style>