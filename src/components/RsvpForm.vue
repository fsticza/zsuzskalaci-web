<template>
  <form novalidate @submit.prevent="onSubmit">

    <div class="row">
      <form-group class="col-sm-6">
        <label>Neved:</label>
        <form-control name="name" v-model="name" maxlength="50" minlength="2" required />
        <div class="invalid-feedback">
          Minimum 2, maximum 50 karakter, reméljük ez elég ;)
        </div>
      </form-group>

      <form-group class="col-sm-6">
        <label>E-mail címed:</label>
        <form-control name="email" v-model="email" type="email" required />
        <div class="invalid-feedback">
          Hibás e-mail formátum.
        </div>
      </form-group>
    </div>

    <div class="row">
      <form-group class="col-sm-6">
        <label>Erre a részre mennék:</label>
        <form-control name="event" type="select" v-model="event" required :options="attendingOptions"
          placeholder="Kérjük, válassz!" />
        <div class="invalid-feedback">
          Válassz egy lehetőséget!
        </div>
      </form-group>

      <form-group class="col-sm-6">
        <label>Vendégeim száma:</label>
        <form-control min="0" max="10" name="guests" type="number" required v-model.number="guests" />
        <div class="invalid-feedback">
          Minimum 0, maximum 10 fő.
        </div>
      </form-group>

    </div>

    <form-group>
      <label>Megjegyzés:</label>
      <form-control name="comment" v-model="comment" type="textarea" maxlength="250"
        placeholder="Ételérzékenység, ilyesmi" />
      <div class="invalid-feedback">
        Minimum 250 karakter.
      </div>
    </form-group>

    <alert v-if="result.type" :type="result.type">
      {{result.msg}}
    </alert>

    <div class="text-center">
      <button type="submit" class="btn btn-lg btn-primary">
        Elküldöm
      </button>
    </div>

  </form>
</template>

<script>
import Alert from '@/components/Alert'
import FormGroup from '@/components/form/FormGroup'
import FormControl from '@/components/form/FormControl'
export default {
  name: 'rsvp-form',
  data () {
    return {
      name: '',
      email: '',
      guests: 0,
      event: '',
      comment: '',
      result: {},
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
    onSubmit (ev) {
      this.result = {}
      ev.target.classList.add('was-validated')
      if (!ev.target.checkValidity()) {
        return
      }
      const { name, email, guests, event, comment } = this
      fetch('https://q4xk8cg9d0.execute-api.eu-central-1.amazonaws.com/dev/rsvps', {
        method: 'POST',
        mode: 'cors',
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
        .then(() => {
          this.result = {
            type: 'success',
            msg: 'Köszönjük a visszajelzést! Találkozunk az esküvőn!'
          }
        })
        .catch(() => {
          this.result = {
            type: 'danger',
            msg: 'Hibás vagy hiányzó adatok'
          }
        })
    }
  },
  components: {
    Alert,
    FormGroup,
    FormControl
  }
}
</script>
