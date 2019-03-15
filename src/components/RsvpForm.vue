<template>
  <form @submit.prevent="onSubmit">
    <div class="row">
      <form-group class="col-sm-6">
        <label>Neved:</label>
        <form-control name="name" v-model="name" />
      </form-group>

      <form-group class="col-sm-6">
        <label>E-mail címed:</label>
        <form-control name="email" v-model="email" type="email" />
      </form-group>
    </div>

    <div class="row">
      <form-group class="col-sm-6">
        <label>Erre a részre mennék:</label>
        <form-control name="event" type="select" v-model="event" :options="attendingOptions"
          placeholder="Kérjük válassz!" />
      </form-group>

      <form-group class="col-sm-6">
        <label>Vendégeim száma:</label>
        <form-control min="0" max="10" name="guests" type="number" v-model.number="guests" />
      </form-group>

    </div>

    <form-group>
      <label>Megjegyzés:</label>
      <form-control name="comment" v-model="comment" type="textarea"
        placeholder="Ételérzékenység, ilyesmi" />
    </form-group>

    <div class="text-center">
      <button type="submit" class="btn btn-lg btn-primary">
        Elküldöm
      </button>
    </div>

  </form>
</template>

<script>

import FormGroup from '@/components/form/FormGroup'
import FormControl from '@/components/form/FormControl'
export default {
  name: 'rsvp-form',
  data () {
    return {
      name: '',
      email: '',
      guests: 0,
      event: 0,
      comment: '',
      attendingOptions: [
        {
          label: 'Egyházi ceremónia',
          value: 1
        },
        {
          label: 'Vacsora & Party',
          value: 2
        },
        {
          label: 'Mindkettő',
          value: 3
        }
      ]
    }
  },
  methods: {
    onSubmit () {
      const { name, email, guests, event, comment } = this
      fetch('http://localhost:3000/rsvps', {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
          'Accept': 'application/json; charset=UTF-8'
        },
        body: JSON.stringify({
          name,
          email,
          guests,
          event,
          comment
        })
      })
    }
  },
  components: {
    FormGroup,
    FormControl
  }
}
</script>
