<template>
    <div>
        <b-container>
            <b-alert variant="danger" show>All players and coaches <strong>MUST</strong> have a verified NACCS account. Click HERE to learn how.</b-alert>
            <b-row>
                <b-col>
                    <b-card img-src="@/assets/background.jpg" img-alt="Card image" img-top class="shadow p-3 mb-5 bg-white rounded border-primary">
                    <b-card-text>
                        rules, regulations and whatever else goes here.
                    </b-card-text>
                    </b-card>
                </b-col>
                <b-col>
                <b-card class="shadow p-3 mb-5 bg-white rounded border-primary" border-variant="primary" header="Registration Form" header-border-variant="primary">
    <b-form @submit="onSubmit" @reset="onReset" v-if="show">
      <b-form-group
        id="input-group-1"
        label="Contact Email:"
        label-for="input-1"
        description="Email address where confirmation and payment info will be sent."
      >
        <b-form-input
          id="input-1"
          v-model="form.email"
          type="email"
          required
          placeholder="Enter email"
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-2" label="Captain / Player 1 NACCS User Name:" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.players.p1name"
          required
          placeholder="Enter username"
        ></b-form-input>
      </b-form-group>

        <b-form-group id="input-group-3" label="Player 2 NACCS User Name:" label-for="input-3">
        <b-form-input
          id="input-3"
          v-model="form.players.p2name"
          required
          placeholder="Enter username"
        ></b-form-input>
      </b-form-group>

        <b-form-group id="input-group-4" label="Player 3 NACCS User Name:" label-for="input-4">
        <b-form-input
          id="input-4"
          v-model="form.players.p3name"
          required
          placeholder="Enter username"
        ></b-form-input>
      </b-form-group>

        <b-form-group id="input-group-5" label="Player 4 NACCS User Name:" label-for="input-5">
        <b-form-input
          id="input-5"
          v-model="form.players.p4name"
          required
          placeholder="Enter username"
        ></b-form-input>
      </b-form-group>

        <b-form-group id="input-group-6" label="Player 5 NACCS User Name:" label-for="input-6">
        <b-form-input
          id="input-6"
          v-model="form.players.p5name"
          required
          placeholder="Enter username"
        ></b-form-input>
      </b-form-group>

        <b-form-group id="input-group-7" label="Coach NACCS User Name:" label-for="input-7" description="Not required.">
        <b-form-input
          id="input-7"
          v-model="form.coach"
          placeholder="Enter username"
        ></b-form-input>
      </b-form-group>


      <b-button type="submit" pill variant="outline-primary">Submit</b-button>
    </b-form>
                </b-card>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
  export default {
    data() {
      return {
        form: {
          email: '',
          coach: '',
          players: {
            p1name: '',
            p2name: '',
            p3name: '',
            p4name: '',
            p5name: ''
          },
        },
        show: true
      }
    },
    methods: {
      onSubmit(evt) {
        evt.preventDefault()
        alert(JSON.stringify(this.form))
        console.log(JSON.stringify(this.form))
      }
    }
  }
</script>