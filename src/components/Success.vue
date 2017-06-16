<template>
  <div>
    <h3>Sukses Login dengan Data</h3>
    <table>
      <tr>
        <th>Email</th>
        <td>:</td>
        <td>{{email}}</td>
      </tr>
      <tr>
        <th>Omni Key</th>
        <td>:</td>
        <td>{{omniKey}}</td>
      </tr>
      <tr>
        <th>Token</th>
        <td>:</td>
        <td>{{token}}</td>
      </tr>
      <tr>
        <th>User ID</th>
        <td>:</td>
        <td>{{user_id}}</td>
      </tr>
      <tr>
        <th>Username</th>
        <td>:</td>
        <td>{{username}}</td>
      </tr>
    </table>
  </div>
</template>

<script>
  export default {
    name: 'success',
    data () {
      return {
        email: '',
        omniKey: '',
        token: '',
        user_id: '',
        username: ''
      }
    },
    created () {
      var dataauth = JSON.parse(window.localStorage.getItem('auth_item'))
      console.log('Init data')
      console.log(dataauth)
      if (dataauth != null) {
        this.email = dataauth.email
        this.omniKey = dataauth.omniKey
        this.token = dataauth.token
        this.user_id = dataauth.user_id
        this.username = dataauth.username
      }
    }
  }
</script>
