<template>
  <q-page class="flex flex-center">
    <img alt="Quasar logo" src="~assets/quasar-logo-full.svg">
    <q-btn color="primary" icon="check" label="OK" @click="onClick" />
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  methods: {
    onClick () {
      Email.send({
          Host : "smtp.elasticemail.com",
          Username : "darksiege32@gmail.com",
          Password : "c59a3568-90bd-4e31-ad96-7f8467d5826d",
          To : 'jonel.recto@gmail.com',
          From : "darksiege32@gmail.com",
          Subject : "This is the test email notif",
          Body : '<html><body> <p> hey this is a span! </p></body></html>'
      }).then(resp => {
        console.log(resp, 'resp')
      }).catch(err => {
        console.log(err, 'err')
      })
    }
  }
}
</script>
