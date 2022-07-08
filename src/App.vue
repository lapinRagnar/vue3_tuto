<template >
  <div>
    <pre>
      {{ JSON.stringify(formValues, null, 2)}}
    </pre>
  </div>

  <form @submit.prevent="submitForm">
    <div>
      <label for="name">name</label>
      <input type="text" id="name" v-model.trim.lazy="formValues.name">
    </div>

    <div>
      <label for="profile">commentaire du profile</label>
      <textarea name="profile" id="profile" cols="30" rows="10" v-model.trim.lazy="formValues.profileSummary"></textarea>
    </div>

    <div>
      <label for="country">country</label>
      <select name="country" id="country" v-model="formValues.country">
        <option value="">votre pays</option>
        <option value="france">france</option>
        <option value="allemagne">allemagne</option>
        <option value="angleterre">angleterre</option>
      </select>
    </div>

    <div>
      <label for="job-location">Lieu de travail</label>
      <select name="job-location" id="job-location" multiple v-model="formValues.jobLocation">
        <option value="">votre pays</option>
        <option value="france">france</option>
        <option value="allemagne">allemagne</option>
        <option value="angleterre">angleterre</option>
      </select>
    </div>

    <div>
      <input type="checkbox" id="remoteWork" v-model="formValues.remoteWork" true-value="yes" false-value="no">
      <label for="remoteWork">Deplacement ?</label>
    </div>

    <div>
      <label>competence</label>
      <input type="checkbox" name="html" id="html" value="html" v-model="formValues.skillSet">
      <label for="html">HTML</label >
      <input type="checkbox" name="css" id="css" value="css" v-model="formValues.skillSet">
      <label for="css">CSS</label>
      <input type="checkbox" name="javascript" id="javascript" value="javascript" v-model="formValues.skillSet">
      <label for="javascript">JavaScript</label>      
    </div>

    <div>
      <label >Année d'experience</label>
      <input type="radio" name="0-2" id="0-2" value="0-2" v-model="formValues.yearsOfExperience">
      <label for="0-2">0-2</label>
      <input type="radio" name="3-5" id="3-5" value="3-5" v-model="formValues.yearsOfExperience">
      <label for="3-5">3-5</label>
      <input type="radio" name="6-10" id="6-10" value="6-10" v-model="formValues.yearsOfExperience">
      <label for="6-10">6-10</label>
      <input type="radio" name="10+" id="10+" value="10+" v-model="formValues.yearsOfExperience">
      <label for="10+">10+</label>
    </div>

    <div>
      <label for="age">age</label>
      <input type="number" name="age" id="age" v-model.number="formValues.age">
    </div>

    <div>
      <button>Valider</button>
    </div>

  </form>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      formValues: {
        name:'',
        profileSummary: '',
        country: '',
        jobLocation: [],
        remoteWork: 'no',
        skillSet: [],
        yearsOfExperience: '',
        age: null
      }
    }    
  },
  methods: {
    submitForm(){
      console.log('formulaire', this.formValues);
    }
  }
}
</script>

<style>

label{
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
}

input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}

input[type='text'], 
textarea,
select{
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.42;
  color: #555;
  background-color: #fff;
  background-image: none;
}

#app {

  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}


</style>
